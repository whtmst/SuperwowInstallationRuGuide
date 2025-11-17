# Руководство по установке Superwow
<hr>

![image](https://github.com/whtmst/SuperwowInstallationRuGuide/blob/main/img/1.png)

### 1. Отключите защиту в реальном времени в Windows (она автоматически включится через некоторое время), так как она блокирует загрузку VanillaFixes и superwow.
<hr>

![image](https://github.com/whtmst/SuperwowInstallationRuGuide/blob/main/img/2.png)

### 2. Пока открыт центр безопасности Windows, добавьте исключение для папки с Turtle WoW (там, где находится WoW.exe), чтобы защита не удалила VanillaFixes/superwow в будущем.
<hr>

### 3A. Если вы планируете использовать лаунчер Turtle WOW:
#### 1. Перейдите на вкладку аддонов и добавьте аддон [SuperAPI](https://github.com/balakethelock/SuperAPI)
#### 2. Перейдите к [шагу 6](https://github.com/whtmst/SuperwowInstallationRuGuide?tab=readme-ov-file#6-%D1%81%D0%BA%D0%B0%D1%87%D0%B0%D0%B9%D1%82%D0%B5-%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%D0%B4%D0%BD%D1%8E%D1%8E-%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8E-superwow-dll-%D0%BE%D1%82%D1%81%D1%8E%D0%B4%D0%B0-httpsgithubcombalakethelocksuperwowreleasestagrelease-%D0%B8-%D0%BF%D0%BE%D0%BC%D0%B5%D1%81%D1%82%D0%B8%D1%82%D0%B5-%D0%B2-%D0%BF%D0%B0%D0%BF%D0%BA%D1%83-%D1%81-turtle-wow-%D1%80%D1%8F%D0%B4%D0%BE%D0%BC-%D1%81-wowexe-%D0%B2%D0%B0%D0%BC-%D0%BD%D1%83%D0%B6%D0%B5%D0%BD-%D1%82%D0%BE%D0%BB%D1%8C%D0%BA%D0%BE-%D1%84%D0%B0%D0%B9%D0%BB-dll---superwowhookdll-%D0%BB%D0%B0%D1%83%D0%BD%D1%87%D0%B5%D1%80-superwowlauncherexe-%D0%BD%D0%B5-%D0%BD%D1%83%D0%B6%D0%B5%D0%BD)
<br/>

### 3B. Если НЕ используете лаунчер Turtle WOW: 
Скачайте последнюю версию Vanilla Fixes (версия 1.4 или выше), если у вас её ещё нет, отсюда: https://github.com/hannesmann/VanillaFixes/releases и поместите файл в папку с Turtle WoW рядом с WoW.exe.

Если при переключении между окнами у вас появляется чёрный экран, добавьте строку `d3d9.enableDialogMode = True` в файл dxvk.conf.
<hr>

### 4. (Опционально) Если вы хотите также установить VanillaTweaks:
- Скачайте их отсюда: https://github.com/brndd/vanilla-tweaks?tab=readme-ov-file#current-patches и поместите в папку с Turtle WoW рядом с WoW.exe
- Сделайте копию файла `WoW.exe` (на всякий случай)
- Перетащите `WoW.exe` на `vanilla_tweaks.exe` ИЛИ запустите команду `./vanilla-tweaks WoW.exe` из командной строки в папке, где лежат `WoW.exe` и `vanilla-tweaks.exe`. Если вы хотите указать конкретные настройки (например, увеличение дистанции отображения индикаторов здоровья), используйте командную строку. Смотрите примеры здесь: https://github.com/brndd/vanilla-tweaks?tab=readme-ov-file#usage
- Переименуйте `WoW_tweaked` в `WoW` ИЛИ `WoW_tweaked.exe` в `WoW.exe` (в зависимости от того, включено ли в Windows отображение расширений файлов). Будьте внимательны, чтобы случайно не получить файл с именем `WoW.exe.exe`, если отображение расширений выключено.
<hr>

### 5. Скачайте последнюю версию аддона SuperWoW API отсюда: https://github.com/balakethelock/SuperAPI и поместите его в папку `Interface/Addons`, убедившись, что убрали суффикс "-master", который добавляет GitHub.

В иконке на миникарте, которую добавляет этот аддон, вы можете настроить следующие параметры:
- Автоматический сбор добычи
- Сквозное нажатие по надгробиям
- Звук в фоновом режиме
- Лимит звуков
- Поле зрения
- Стиль выделения целей
<hr>

### 6. Скачайте последнюю версию SuperWoW DLL отсюда: https://github.com/balakethelock/SuperWoW/releases/tag/Release и поместите в папку с Turtle WoW рядом с WoW.exe. Вам нужен ТОЛЬКО файл DLL - SuperWoWhook.dll, лаунчер SuperWoWlauncher.exe НЕ нужен.
<hr>

### 7A. Если используете лаунчер Turtle WOW, включите мод SuperWoWhook на вкладке модов. Это добавит его в файл dlls.txt и предотвратит его удаление при последующих запусках.

### 7B. Если НЕ используете лаунчер, убедитесь, что `SuperWoWhook.dll` указан в вашем файле `dlls.txt`. Этот файл находится в папке с Turtle WoW рядом с WoW.exe.

Если вы используете VanillaFixes, он уже должен быть там. Порядок не имеет значения. Вот пример содержимого моего файла dlls.txt:

![image](https://github.com/whtmst/SuperwowInstallationRuGuide/blob/main/img/3.png)

<hr>

### 8. (Опционально) Если вы хотите видеть улучшенные полосы заклинаний противников, выберите ОДИН из вариантов:
<b>НЕ ИСПОЛЬЗУЙТЕ оба варианта вместе.</b>

#### Вариант 1: PFUI
Скачайте последнюю версию PFUI отсюда: https://github.com/shagu/pfUI и поместите в папку `Interface/Addons`, убедившись, что убрали суффикс "-master", который добавляет GitHub.

#### Вариант 2: SuperAPI_Castlib
Скачайте последнюю версию аддона SuperWoW castlib отсюда: https://github.com/balakethelock/SuperAPI_Castlib и поместите в папку `Interface/Addons`, убедившись, что убрали суффикс "-master", который добавляет GitHub.
<hr>

### 9. Если используете лаунчер Turtle WOW, запускайте игру через него. В противном случае запускайте игру через `VanillaFixes.exe`. При первом запуске должно появиться окно со списком загружаемых DLL, и SuperWoW должен быть среди них.
<hr>

### 10. В игре откройте окно создания макроса. Если у вас доступно 512 символов для макроса — SuperWoW работает корректно.
<hr>

### 11. (Опционально) Пропустите этот шаг, если уже сделали это при установке SuperAPI. Если вы использовали VanillaTweaks для работы звука, когда игра свёрнута, выполните команду `/run SetCVar("BackgroundSound", "1")`, чтобы снова включить эту функцию. Также можно выполнить `/run SetCVar("UncapSounds", "1");SetCVar("SoundMaxHardwareChannels", "64");SetCVar("SoundSoftwareChannels", "64");`, чтобы позволить игре воспроизводить больше звуков одновременно.

Другие CVar'ы и функции можно посмотреть здесь: https://github.com/balakethelock/SuperWoW/wiki/Features

### 12. Если при запуске вы получаете одну из этих ошибок:
![image](https://github.com/whtmst/SuperwowInstallationRuGuide/blob/main/img/4.png)
![image](https://github.com/whtmst/SuperwowInstallationRuGuide/blob/main/img/5.png)

В Windows: Перейдите в Панель управления > Система и безопасность > Система > Дополнительные параметры системы. В разделе "Быстродействие" нажмите "Параметры", затем перейдите на вкладку "Предотвращение выполнения данных".

Выберите "Включить DEP для всех программ и служб, кроме выбранных ниже" и добавьте `WoW.exe` в список исключений. (Не забудьте убрать его оттуда позже, если это не помогло.)

Эта ошибка также может быть вызвана отсутствием распространяемых пакетов Visual C++. Попробуйте установить их по этим ссылкам:

32-битная версия (x86): https://aka.ms/vs/17/release/vc_redist.x86.exe (скорее всего, нужна только эта)

64-битная версия (x64): https://aka.ms/vs/17/release/vc_redist.x64.exe
