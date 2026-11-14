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

---

## ✅ Available now / Уже есть — [v1.0.0](../../releases/latest)

Visual overlay editor · text, rotating text, counters (Twitch / YouTube, summed or separate) · countdown timer · stopwatch with a global hotkey · chat · your own SVG backgrounds with per-layer effects · view rotation · templates · start with Windows or with OBS / Streamlabs · English / Russian.

Визуальный редактор оверлеев · тексты, сменяющиеся тексты, счётчики (Twitch / YouTube, суммой или по отдельности) · таймер обратного отсчёта · секундомер с глобальной клавишей · чат · свои SVG-фоны с эффектами по слоям · ротация видов · шаблоны · автозапуск с Windows или с OBS / Streamlabs · английский / русский.

Support the project / поддержать проект: **[Boosty](https://boosty.to/krogosh/donate)**
