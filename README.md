# WSD — Панель саморазвития для Android

Это Android Studio-проект, созданный на основе текущего HTML-файла `WSD (1).html`.

## Как это устроено

Приложение использует нативную Android-оболочку с `WebView`, внутри которой запускается исходный HTML как локальный asset:

`app/src/main/assets/WSD.html`

JavaScript, CSS и локальное хранение данных остаются внутри HTML. Используемые `localStorage`-данные сохраняются в хранилище WebView приложения.

## Сборка APK

1. Откройте папку проекта в Android Studio.
2. Дождитесь синхронизации Gradle.
3. Выполните `Build → Build APK(s)`.
4. Полученный debug APK будет находиться примерно здесь:
   `app/build/outputs/apk/debug/app-debug.apk`

Для релизной публикации можно создать подписанный APK/AAB через `Build → Generate Signed Bundle / APK`.

## Требования

- Android Studio с Android SDK
- Android SDK Platform 35
- JDK 17+
- Gradle скачивается Android Studio автоматически

## Важно

В этой среде Android SDK/build-tools отсутствуют, поэтому сам APK здесь не был скомпилирован. Проект подготовлен для непосредственного открытия и сборки в Android Studio.

### Иконка приложения

В проект добавлена простая иконка WSD: адаптивный вариант для Android 8+ и отдельные PNG-ресурсы для mdpi/hdpi/xhdpi/xxhdpi/xxxhdpi. Для круглых лаунчеров также задан `ic_launcher_round`.
