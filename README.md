# Slug City (Cordova + PWA)
Готовый проект для сборки APK и установки как PWA.

## Быстрый старт как PWA (без магазина)
1) Поднимите локальный сервер в папке `www`:
   - Python: `python -m http.server 8080`
   - или Node: `npx serve www -l 8080`
2) Откройте http://localhost:8080, нажмите «Установить»/«Добавить на главный экран» — получите иконку на телефоне.

## Сборка APK (Cordova)
0) Установите: Node.js LTS, Java JDK 17, Android Studio (SDK + Platform Tools).
1) Установите Cordova: `npm i -g cordova`
2) В корне проекта:
   - `cordova platform add android`
   - `cordova build android`
3) APK появится в `platforms/android/app/build/outputs/apk/debug/app-debug.apk`.

Советы:
- Если нужен портретный режим — поменяйте `<preference name="Orientation" value="landscape" />` в `config.xml`.
- Картинки/иконки кладите в `www/assets/` и подключайте в `index.html`.
