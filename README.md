# 🎨 Podnikový informační systém — Frontend (Klientský modul)

Tento repozitář obsahuje čistě klientskou část aplikace napsanou v **HTML5, moderním CSS a čistém asynchronním JavaScriptu (Fetch API)**.

Frontend poskytuje uživatelské rozhraní pro aplikaci umožňující zadávat informace o projektech (název, popis, datum zahájení, datum ukončení, stav projektu, členy projektového týmu). 
Název projektu musí být unikátní. Stav projektu může nabývat jedné z hodnot ve statickém select boxu (Příprava, V realizaci, Pozastaven, Dokončen).
Dále lze registrovat osoby, které se mohou účastnit projektů, tj. mohou být členy projektových týmů. U osoby se ukládá jméno, příjmení, email a pozice.
Email musí být unikátní. 

Design uživatelského rozhraní:
- levý frame (sloupec) je určen pro správu projektů, přičemž v horní části lze provádět filtrování záznamů, které se zobrazují uživateli v tabulce níže.
- u každého vyhledaného záznamu jsou ve sloupečku "AKCE" dvě tlačítka pro operace UPDATE a DELETE.
- UPDATE načte záznam do formuláře pod tabulkou. Formulář slouží nejen pro aktualizace existujících záznamů, ale i pro vkládání nových záznamů 
- POZOR: DELETE provádí fyzické smazání z databáze !!

- pravý frame (sloupec) je určen pro správu osob účastnících se na projektech. Je uspořádán analogicky a nabízí podobné funkce jako levý sloupec. 

### 🔗 Propojení
* **Backend repozitář najdete zde:** [https://github.com/cestmirstrmiska/evidence-projektu-backend.git]

### 🚀 Jak spustit frontend lokálně:
1. Ujistěte se, že vám na pozadí běží backend na portu 8000.
2. Otevřete soubor `index.html` v libovolném webovém prohlížeči (nebo přes Live Server v PyCharmu).
Frontend komunikuje asynchronně s API na adrese `http://127.0.0.1:8000/api`.
