# KW-NoCheat-Brutal-Overlord-AI (Command & Conquer 3: Kane's Wrath)

Оригинальный агрессивный ИИ **«Владыка» (Overlord / Steamroller)** на сложности **«Генерал» (Brutal)** для **всех 9 фракций и подфракций**, но с **честной экономикой (100% дохода)** вместо читерских 200%.

*Based on the build pipeline by [bquenin/commander](https://github.com).*

---

## Что именно меняет этот мод / What this mod does

В стандартной версии *Kane's Wrath* ИИ на сложности **«Генерал» (Brutal)** получает скрытый **двойной бонус к деньгам (`200%`)** с каждого комбайна, из-за чего заваливает игрока бесконечными толпами войск.

Этот мод берёт за основу оригинальные агрессивные профили **«Владыки» (`5...Overlord`)** из базовой игры (с их танковыми дебютами, быстрым выходом в тяжёлую технику и графиками технологий), но меняет множитель ресурсов с `200%` на **`100%`**.

* **Поддерживаются все 9 фракций:** ГСБ (GDI), Стальные Когти (Steel Talons), ЗОКОМ (ZOCOM), Братство Нод (Nod), Чёрные Братья (Black Hand), Избранные Кейна (Marked of Kane), Скринны (Scrin), Жнецы-17 (Reaper-17), Странники-59 (Traveler-59).
* **Честный баланс 1 к 1:** Бот платит столько же кредитов и тратит столько же времени на постройку зданий и юнитов, сколько и игрок.
* **Все нужные утилиты уже внутри:** В архиве `commander-main.zip` уже лежат скомпилированные XML-профили и инструменты `WrathEd` / `MakeBig`.

---

## Подробная установка (для русской и английской версий)

1. **Скачайте архив:** Нажмите на файл **`commander-main.zip`** выше и нажмите кнопку скачивания (**Download raw file**).
2. **Распакуйте архив** в любую удобную папку (например, `D:\KW_Fair_AI`).
3. **Откройте PowerShell в распакованной папке:**
   * Зайдите в папку `commander-main` (где лежит файл `BuildModKW.ps1`).
   * Нажмите левой кнопкой мыши на пустое место в **адресной строке проводника** вверху, напишите **`powershell`** и нажмите **Enter** — откроется синее окно терминала прямо в этой папке.
4. **Запустите автоматическую сборку и установку:**
   * **Для русской версии игры** вставьте в окно PowerShell эту команду и нажмите **Enter**:
     ```powershell
     powershell -ExecutionPolicy Bypass -File .\BuildModKW.ps1 -Language russian
     ```
   * **Для английской версии игры** используйте эту команду:
     ```powershell
     powershell -ExecutionPolicy Bypass -File .\BuildModKW.ps1 -Language english
     ```
   * *(Примечание: если скрипт напишет, что не нашёл папку с игрой в реестре, укажите путь к игре вручную в конце команды, например:*
     `powershell -ExecutionPolicy Bypass -File .\BuildModKW.ps1 -Language russian -GamePath "D:\Games\Command and Conquer 3 - Kanes Wrath"` *).*
5. **Дождитесь зелёной надписи `Done.`** — скрипт сам создаст конфиг патча `1.3.SkuDef` в папке с игрой, поэтому **никакие сторонние лаунчеры не нужны**.

---

## Как запустить бой против честного «Владыки»

1. Запустите игру с **обычного ярлыка** на рабочем столе.
2. Зайдите в режим **Схватка (Skirmish)**.
3. Выберите сопернику любую из 9 фракций, сложность поставьте **«Генерал» (Brutal)**, а в графе **Характер ИИ (AI Personality)** выберите новый пункт в самом низу списка:
   * **`Commander`** (в русской версии может отображаться как **`MISSING: 'Personality:Comm...'`** — это нормально, профиль полностью рабочий).
4. Начинайте матч!

---

## Как удалить мод и вернуть чистую версию 1.2

Откройте PowerShell в той же папке `commander-main` и выполните команду:
```powershell
powershell -ExecutionPolicy Bypass -File .\UninstallModKW.ps1
```
Скрипт удалит созданный файл `1.3.SkuDef`, и игра вернётся в исходное состояние.

---

## English Quick Guide

1. Download and extract **`commander-main.zip`**.
2. Open PowerShell inside the extracted `commander-main` folder (type `powershell` in the File Explorer address bar and press **Enter**).
3. Run the build script:
   ```powershell
   powershell -ExecutionPolicy Bypass -File .\BuildModKW.ps1 -Language english
   ```
   *(If the game path is not detected automatically, add `-GamePath "C:\Path\To\Kanes Wrath"`).*
4. Launch the game normally, go to **Skirmish**, set AI difficulty to **Brutal**, and set AI Personality to **`Commander`** (or `MISSING: 'Personality:Commander'`).
5. To uninstall at any time, run `.\UninstallModKW.ps1` in PowerShell.

