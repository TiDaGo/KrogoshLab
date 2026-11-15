# Roadmap / План развития

What is planned for KrogosLab. Order and scope may change — ideas and feedback are welcome in [Issues](../../issues).
Что планируется в KrogosLab. Порядок и состав могут меняться — идеи и отзывы оставляйте в [Issues](../../issues).

**Status / Статус:** 🔜 planned / запланировано · 🛠 in progress / в работе · ✅ done / готово

---

## 🔜 1. Chat text-to-speech / Озвучка чата

Read chat messages aloud with Windows voices — no extra software.
Чтение сообщений чата вслух голосами Windows — без сторонних программ.

- Voice, speed and volume; separate voices per platform / голос, скорость и громкость; свои голоса для разных площадок
- Filters: skip commands (`!…`), links, emotes-only and too long messages; read only selected users or roles / фильтры: пропуск команд (`!…`), ссылок, сообщений из одних смайлов и слишком длинных; чтение только выбранных пользователей или ролей
- Queue with a hotkey to skip or pause / очередь с горячей клавишей «пропустить» / «пауза»
- “Name says: …” template / шаблон «Имя пишет: …»

## 🔜 2. Donation alerts / Оповещения о донатах

On-screen alerts for donations and support events, built in the same editor as the rest of the overlay.
Оповещения о донатах и поддержке на экране — настраиваются в том же редакторе, что и весь оверлей.

- Sources: DonationAlerts, Twitch (subs, gifted subs, bits, raids), YouTube (Super Chat, memberships) — more on request / источники: DonationAlerts, Twitch (подписки, подарочные подписки, биты, рейды), YouTube (Super Chat, спонсорство) — другие по запросу
- Alert = image / animation + sound + text template (`{name}`, `{amount}`, `{message}`) / оповещение = картинка или анимация + звук + шаблон текста (`{name}`, `{amount}`, `{message}`)
- Variants by amount (e.g. a bigger alert from 500 ₽) / разные варианты по сумме (например, крупное оповещение от 500 ₽)
- Reading the donation message aloud (uses the text-to-speech above) / озвучка сообщения доната (на основе озвучки чата)
- Queue so alerts never overlap; test button in the editor / очередь, чтобы оповещения не накладывались; кнопка «тест» в редакторе

## 🔜 3. Voice-reactive avatar (PNGTuber) / Аватар, реагирующий на голос (PNGTuber)

A character on stream that “talks” when you talk: images switch by your microphone level.
Персонаж на стриме, который «говорит», когда говорите вы: картинки меняются по уровню звука с микрофона.

- Images: idle, talking, optionally blinking and “shouting” (loud) / изображения: молчит, говорит, по желанию моргание и «крик» (громко)
- Microphone choice, sensitivity threshold and smoothing so the avatar doesn’t flicker / выбор микрофона, порог чувствительности и сглаживание, чтобы аватар не дёргался
- Bounce / shake effects while talking, using the existing effects / подпрыгивание или покачивание во время речи — на основе уже существующих эффектов
- Expression sets switched by hotkeys (happy, angry, …) / наборы эмоций, переключаемые горячими клавишами (радость, злость, …)
- *Later:* face tracking from a webcam (VTuber-style) is being considered / *позже:* рассматривается отслеживание лица по веб-камере (как у VTuber)

## 🔜 4. Keyboard & mouse display / Отображение нажатий клавиш и мыши

Show which keys and mouse buttons you press — for gameplay tutorials, speedruns and rhythm games.
Показ нажимаемых клавиш и кнопок мыши — для обучающих видео, спидранов и ритм-игр.

- Layouts: WASD + mouse, full keyboard, gamepad-style, custom keys on your own SVG / раскладки: WASD + мышь, полная клавиатура, геймпад, свои клавиши на своём SVG
- Pressed-key highlight, press counter (APM / KPS) / подсветка нажатой клавиши, счётчик нажатий (APM / KPS)
- **Privacy:** only the keys you choose are shown, nothing is recorded or sent anywhere; a hotkey hides the display instantly (e.g. while typing a password) / **конфиденциальность:** показываются только выбранные вами клавиши, ничего не записывается и никуда не отправляется; горячая клавиша мгновенно скрывает показ (например, при вводе пароля)

## 🔜 5. Live bilingual subtitles RU ⇄ EN / Живые двуязычные субтитры RU ⇄ EN

Speech recognition and translation shown as subtitles — for streams with foreign viewers or guests. Designed to run free of charge, even on a busy or modest PC.
Распознавание речи и перевод в виде субтитров — для стримов с иностранными зрителями или гостями. Задумано бесплатным, в том числе на загруженном или слабом ПК.

- Two audio sources at once: your microphone and a guest (Discord or any other app — captured per application, so game sound and music stay out) / два источника звука одновременно: ваш микрофон и гость (Discord или другая программа — звук захватывается отдельно, игра и музыка в субтитры не попадают)
- Automatic language detection RU / EN per phrase and translation in the right direction: Russian → English, English → Russian / автоопределение языка RU / EN для каждой фразы и перевод в нужную сторону: русский → английский, английский → русский
- Choice of engine / выбор движка:
  - **Cloud** (Groq / Azure free tiers, your own key) — best quality, almost no load on the PC / **облако** (бесплатные тарифы Groq / Azure, ваш ключ) — лучшее качество, почти без нагрузки на ПК
  - **Local light** (Vosk + Opus-MT) — offline, runs on modest hardware / **локальный лёгкий** (Vosk + Opus-MT) — без интернета, работает на слабом железе
  - **Local Whisper** — offline, high quality for PCs with a good GPU / **локальный Whisper** — без интернета, высокое качество для ПК с хорошей видеокартой
- Automatic fallback: if the cloud is unavailable or the free limit runs out, subtitles switch to the local engine instead of disappearing / автоматическое переключение: если облако недоступно или бесплатный лимит исчерпан, субтитры переходят на локальный движок, а не пропадают
- Subtitles widget in the editor: speaker names and colors, original + translation or translation only, fonts, backgrounds and effects as in other widgets / виджет «Субтитры» в редакторе: имена и цвета говорящих, оригинал + перевод или только перевод, шрифты, фоны и эффекты как у остальных виджетов
- Duplicate filter for guest speech picked up by the microphone from speakers / фильтр дублей, если микрофон слышит гостя из колонок
- API keys are stored only in KrogosLab and never shown in the browser / ключи API хранятся только в KrogosLab и не показываются в браузере

---

## ✅ Available now / Уже есть — [v1.0.0](../../releases/latest)

Visual overlay editor · text, rotating text, counters (Twitch / YouTube, summed or separate) · countdown timer · stopwatch with a global hotkey · chat · your own SVG backgrounds with per-layer effects · view rotation · templates · start with Windows or with OBS / Streamlabs · English / Russian.

Визуальный редактор оверлеев · тексты, сменяющиеся тексты, счётчики (Twitch / YouTube, суммой или по отдельности) · таймер обратного отсчёта · секундомер с глобальной клавишей · чат · свои SVG-фоны с эффектами по слоям · ротация видов · шаблоны · автозапуск с Windows или с OBS / Streamlabs · английский / русский.

Support the project / поддержать проект: **[Boosty](https://boosty.to/krogosh/donate)**
