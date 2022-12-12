# pyscript_dokumentacio
### Alap pyscripes weboldal létrehozása ami egy fáljt beolvas és adatait kiirja

* A Pyscript meghivása a head-ben --> link: https://pyscript.net/  

* HTML weboldalon belül a body-ba py-script -en belül berakjunk a kodonkat

* beimportáljuk pyodide.http-ből az open-url-t

* létrehozunk egy class-t

* with open_url-el megnyitunk egy githubon tárolt txt fáljt

* beolvassuk a fáljt classel és bele rakjuk egy listába

from pyodide.http import open_url

class Adatbazis:
      def __init__(self,sor):
           ev,elem,vegyjel,rendszam,felfedezo,atomtomeg,negativitas = sor.strip().split(";")
            self.ev = ev
            self.elem = elem
            self.vegyjel = vegyjel
            self.rendszam = rendszam
            self.felfedezo = felfedezo
            self.atomtomeg = atomtomeg
            self.negativitas = negativitas
       
with open_url("https://raw.githubusercontent.com/loczylevi/Kemiai_Elemek/main/tablazat.txt") as f:
        f.readline()
        lista = [Adatbazis(sor) for sor in f]

