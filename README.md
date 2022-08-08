# Az igék csoportosítása az igekötők argumentumszerkezetben okozott változása alapján
## AlkNyelvDok22
### Gyulai Lívia

Absztrakt: A jelen tanulmányban bemutatott kutatás középpontjában az igekötők argumentumszerkezetre való hatása áll, melyben az el igekötő 85 igével való összekapcsolódását vizsgáltam automatikus szintaktikai elemzéssel ellátott korpuszadatok alapján. Hipotézisem szerint az igéket klaszteranalízis segítségével csoportosítani lehet az alapján, hogy az igekötő megjelenése milyen változást okozott az argumentumszerkezetben, így azok az igék fognak egy csoportba kerülni, amelyeknél az igekötő hasonló mértékű hatással volt bizonyos bővítménytípusokra. Az alkalmazott K-means klaszterezés esetlegességének kiküszöbölése érdekében egy ún. hőtérkép is készült, mely alapján megállapítható, hogy milyen bizonyossággal kerülnek az egyes igepárok egy csoportba. A bemutatott módszerrel bármely igekötő argumentumszerkezet-változtató hatásait lehet vizsgálni korpuszból származó adatok alapján automatikus eszközök használatának segítségével is.

A repozitórium a következő fájlokat tartalmazza:

1. **nyers adatok**: Excel fájl, amelynek első munkalapján az igék igekötő nélküli argumentumszerkezeti vektorai;

  második munkalapján az *el* igekötős argumentumszerkezeti vektorok;

  harmadik munkalapján pedig ezen gyakorisági értékek különbsége látható.

2. **el-diff0.tsv**: ez a fájl a nyers adatok harmadik munkalapján található adatokat tartalmazza, a **kmeans.ipynb** program bemeneteként szolgál

3. **kmeans.ipynb**: ez a program elvégzi a K-means klaszterezést, bemenete az **el-diff0.tsv** fájl, kimenete ugyanez, csak utána csatolja a klaszterezés eredményét is

4. **el-cluster-diff_all.tsv**: ez a fájl a **kmeans.ipynb** program kimenete, itt található az **el-diff0.tsv** fájl után csatolt K-means klaszterezés eredménye, a klaszterszámok 2-19-ig terjednek egyes lépésküszöbbel

5. **el-clusters-diff-all-seed0.xlsx**: az **el-cluster-diff_all.tsv** fájl adatai Excel formátumban, színezzéssel a könnyebb átláthatóság érdekében

6. **kmeans-heatmap.ipynb**: ezzel a programmal készül a hőtérkép, a K-means klaszterezést végzi el a 100-szor, klaszterszám: 5. Bemenete ugyanúgy, mint a **kmeans.ipynb** programnak, az **el-diff0.tsv** fájl

7. **el-cluster-heatmap-5class.tsv**: a **kmeans-heatmap.ipynb** program kimenete, melyben látható, hogy az egyes igepárok milyen gyakran kerültek egy klaszterbe a 100 futtatás alkalmával

8. **heatmap-5class.xlsx**: az  **el-cluster-heatmap-5class.tsv** fájl adatait tartalmazó Excel fájl, színezéssel a klaszterek elkülöníthetőségének érdekében 
 
