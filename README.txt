АвтоПомощник KZ — проект Android Studio

Важно: это исходный Android-проект, который упаковывает текущую HTML-версию приложения в Android WebView. Это НЕ готовый APK. В среде подготовки нет Android SDK/Gradle и нет доступа к сети для скачивания инструментов, поэтому скомпилировать и подписать APK здесь невозможно.

Как получить APK:
1. На компьютере установите Android Studio: https://developer.android.com/studio
2. Распакуйте архив и откройте папку AutoPomoshnikKZ-Android как проект.
3. Разрешите Android Studio установить нужные Android SDK компоненты и дождитесь Gradle Sync.
4. Выберите Build > Build Bundle(s) / APK(s) > Build APK(s).
5. APK появится в app/build/outputs/apk/debug/app-debug.apk.
6. Перенесите app-debug.apk на Android и установите. Для установки может потребоваться разрешить установку приложений из выбранного источника.

Текущие ограничения:
- Это локальная WebView-обёртка: нет общей серверной базы между пользователями.
- Реальные платежи, рекламная сеть, карта/маршруты и публикация в Google Play не подключены.
- Данные приложения работают в пределах возможностей текущего HTML-прототипа.
- Перед публикацией в Google Play нужно проверить актуальные требования магазина и privacy policy.

Application ID: kz.autopomoshnik.app
Version: 1.0.0
Minimum Android: 6.0 (API 23)

Облачная сборка без установки Android Studio на телефон:
1. Создайте репозиторий на GitHub на компьютере/в браузере.
2. Загрузите содержимое этой папки в репозиторий (не сам ZIP-файл, а распакованные файлы).
3. Откройте вкладку Actions и запустите workflow "Build Android APK" через Run workflow.
4. После успешной сборки откройте завершённый запуск и скачайте artifact "AutoPomoshnikKZ-debug-apk".
5. Внутри артефакта будет app-debug.apk.

Для GitHub Actions добавлен workflow .github/workflows/build-apk.yml. Облачная сборка требует аккаунт GitHub и успешного Gradle/SDK sync.
