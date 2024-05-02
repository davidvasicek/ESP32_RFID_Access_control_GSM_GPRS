# RFID přístupový systém založený na ESP32, SPIFFS a GSM/GPRS

Tento projekt je zaměřen na vytvoření přístupového systému pomocí technologií RFID, ESP32 (mikrokontrolér od společnosti Espressif), SPIFFS (SPI Flash File System) a GSM/GPRS modulu pro komunikaci.

## Popis

Cílem tohoto projektu je vytvořit jednoduchý, ale efektivní systém pro správu přístupu pomocí RFID karet. ESP32 bude použit k čtení dat z RFID karet a odesílání informací o přístupu přes GSM/GPRS síť. Data budou ukládána do SPIFFS, což umožní jednoduché a spolehlivé ukládání dat na interní paměťové médium ESP32.

## Funkce

- Čtení dat z RFID 125kHz karet/čipů pomocí ESP32
- Ukládání informací o přístupu do interní paměti (SPIFFS)
- Logování informací o přístupu přes GSM/GPRS síť do Firebase Realtime Databáze s přesným Timestampem
- Možnost vzdálené správy a monitorování přístupového systému (TODO)
- detektce neoprávněného otevření dveří. Tj. bez povoleného přístupu
- Zvukové i světelné výstražní a informační signalizace
- Světelná signalizace diagnostiky

## Požadavky

- Hardware:
  - ESP32 mikrokontrolér
  - RFID čtečka
  - GSM/GPRS modul
    
- Software:
  - Arduino IDE (verze 1.x.x pro instalaci pluginu SPIFFS)
  - ESP32 board package
  - Knihovny:
  -   GSM/GPRS knihovna

## Instalace a použití

1. Stáhněte si zdrojový kód a otevřete jej v Arduino IDE.
2. Připojte ESP32 mikrokontrolér k vašemu počítači.
3. Zapojte obvod dle schématu zapojení
4. Nastavte v kódu správné parametry pro komunikaci s GSM/GPRS modulem a Firebasem (Autentizační údaje do Firebase, API FrDB, APN ...... ) TODO 
5. Nahrajte kód do ESP32 mikrokontroléru.
6. Upravte přístupový soubor s RFID UID tagy.
7. Nahrajte přístupový soubor s RFID UID tagy do flash paměti ESP32 mikrokontroléru (pomocí SPIFFS).
8. Připojte napájení k systému a ověřte jeho funkčnost. (Dostatečné množství energie)

## Příspěvky a rozšíření

Tento projekt je otevřený pro příspěvky a rozšíření. Pokud máte nápady na vylepšení funkcionality systému nebo jste implementovali novou funkcionalitu, rádi přijmeme pull requesty.

## Licence

Tento projekt je licencován pod MIT licencí. Pro více informací si prosím přečtěte soubor LICENSE.
