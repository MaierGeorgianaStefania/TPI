# Monitorizarea inteligentă a sistemelor și aplicațiilor

Aplicație web în Python pentru monitorizarea calculatoarelor, mașinilor virtuale și aplicațiilor, cu istoric, alerte și analiză predictivă. Platforma va fi modulară, cu adaptoare pentru sistemele monitorizate; prima integrare va viza Linux și Docker.

## Senzori software

Procese Python vor colecta date reale și vor simula scenarii de funcționare:

| Categorie | Date urmărite |
| --- | --- |
| Resurse | Utilizare CPU, memorie RAM, spațiu liber pe disc și dimensiunea bazelor de date |
| Aplicații | Starea containerelor, restarturi, disponibilitate HTTP și timp de răspuns |
| Erori | Evenimente și numărul erorilor din loguri |
| Builduri și deploy-uri | Data, versiunea și rezultatul ultimului build, respectiv ultima versiune instalată |
| Backupuri | Data, dimensiunea și rezultatul ultimului backup, cu alertare dacă lipsește sau este prea vechi |

## Arhitectură

**Senzori → Gateway Python → Backend cloud → Dashboard web**

Gateway-ul validează și agregă datele, iar backendul păstrează istoricul și îl expune interfeței web. Procesele comunică prin rețea; backendul va rula pe un server în internet. Informațiile despre builduri, deploy-uri și backupuri vor proveni din integrări cu procesele care le execută.

## Dashboard și interfață conversațională

Dashboardul va afișa valorile curente, grafice istorice, alerte și o cronologie a erorilor, buildurilor, deploy-urilor și backupurilor.

Interfața conversațională va permite întrebări precum:

- „În cât timp se va umple discul?”
- „Ce aplicație a crescut cel mai mult în consum de memorie?”
- „Când au început erorile și ce s-a schimbat atunci?”
- „Am suficient spațiu pentru încă o aplicație?”
- „Care este ultimul build și când s-a făcut ultimul backup?”

Răspunsurile vor folosi datele colectate și analizele predictive, semnalând când informațiile sunt insuficiente.

## Nivel de cunoștințe

| Membru                   | Experiență |
|--------------------------| --- |
| Maier Georgiana Stefania | A studiat Python, networking, sockets, threading și dezvoltare web în cadrul facultății. |
| Lacatus Paul Lucian      | A studiat Python, networking, sockets, threading și dezvoltare web în cadrul facultății și le-a utilizat în activitatea de zi cu zi la locul de muncă. |
