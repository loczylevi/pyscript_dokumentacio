# pyscript_dokumentacio
### Alap pyscripes weboldal létrehozása ami egy fáljt beolvas és adatait kiirja

* A Pyscript meghivása a head-ben --> link: https://pyscript.net/  

* HTML weboldalon belül a body-ba py-script -en belül berakjunk a kodonkat

* beimportáljuk pyodide.http-ből az open-url-t






        from pyodide.http import open_url
       
        
      
        

        with open_url("https://raw.githubusercontent.com/loczylevi/Kemiai_Elemek/main/tablazat.txt") as f:
            f.readline()
            lista = [Adatbazis(sor) for sor in f]

