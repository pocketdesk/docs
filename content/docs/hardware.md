---
title: "Hardware"
weight: 2
---

# Hardware

| Item | Role | Connection |
|---|---|---|
| **Pixel 10 Pro XL** *(today)* / **11 Pro XL** *(tomorrow)* | The computer: desktop mode + Linux VM | — |
| **Viture Beast** | Wearable display, 1920×1200/eye, 120 Hz | USB-C DisplayPort Alt Mode |
| **ProtoArc XK01 TP** *(QWERTY · UK · AZERTY)* | Keyboard + trackpad (replaces the mouse) | Bluetooth (paired in Android) |
| *(optional)* Bluetooth mouse | Dedicated pointer | Bluetooth (in Android) |

## Phone

{{< figure src="/images/products/pixel-9-pro.svg" alt="Google Pixel Pro front render" width="190" caption="*Illustrative* — Pixel 9 Pro render; the 10/11 Pro XL share the family design." attr="Mliu92, CC BY-SA 4.0 (Wikimedia Commons)" attrlink="https://commons.wikimedia.org/wiki/File:Google_Pixel_9_(Obsidian)_front.svg" >}}

The reference device is the largest Pixel Pro: **Pixel 10 Pro XL** now, **Pixel 11
Pro XL** when it ships (~September 2026). Pixel matters here because the **graphical**
Linux Terminal (Wayland + GPU) is, as of 2026, effectively a Pixel feature.

- Pixel 8 / 9 / 10 / 11 all expose **USB-C DisplayPort Alt Mode** → external display.
- Android 16 **Desktop Mode** drives a monitor with windows, a dock, and peripherals.
- External output is typically **1080p / 1440p** (no 4K60 here) — a perfect match for
  the glasses' 1200p panels.

> [!NOTE]
> **Foldables work too — as the _computer_.** The **Pixel 9/10 Pro Fold** and **Samsung
> Galaxy Z Fold** all expose DP Alt Mode (Samsung via DeX; Android 16 Desktop Mode is even
> built on DeX's foundations), so they drive the glasses and run the VM fine. But the inner
> screen is **not** a keyboard substitute — typing on glass kills the eyes-free typing the
> glasses depend on. See the keyboard alternatives below.

> [!WARNING]
> **Pixel 11 Pro XL is unreleased (June 2026).** Leaked highlights: Tensor G6 on TSMC
> 2 nm, new OLED panels, MediaTek M90 modem, *smaller* battery offset by efficiency.
> Re-confirm SoC, battery, USB/DisplayPort and Android version at launch.

## Glasses — Viture Beast

{{< figure src="/images/products/ar-glasses-nreal-light.jpg" alt="XR display glasses kit" width="430" caption="*Illustrative* — Nreal Light (Nreal is XReal's former name). The Beast / Luma Ultra / XReal 1S are different, newer models." attr="Mkkwan, CC BY-SA 4.0 (Wikimedia Commons)" attrlink="https://commons.wikimedia.org/wiki/File:Nreal_Light_Consumer_Kit.jpg" >}}

XR display glasses that present as a **plug-and-play DisplayPort monitor**: one USB-C cable,
no software needed for basic display.

- **1920×1200 per eye**, micro-OLED, **120 Hz**, up to 1250 nits.
- Simulates a large virtual screen (~174" at 4 m), 58° FoV.
- The Pixel sees them as an ordinary external display, so Desktop Mode "just works".

## Keyboard — ProtoArc XK01 TP

{{< figure src="/images/products/foldable-keyboard.jpg" alt="A folding Bluetooth keyboard" width="430" caption="*Illustrative* — Microsoft Universal Foldable Keyboard (a bi-fold). The ProtoArc XK01 TP is a tri-fold with an integrated trackpad." attr="Toshiyuki IMAI, CC BY-SA 2.0 (Wikimedia Commons)" attrlink="https://commons.wikimedia.org/wiki/File:Microsoft_Universal_Foldable_Keyboard_-_25228852970.jpg" >}}

A **tri-fold** Bluetooth keyboard that unfolds to a **true full-size 105-key layout**
(F-row, **dedicated arrow keys**, numpad) with an **integrated trackpad**.

- **3-device Bluetooth 5.1**, USB-C rechargeable.
- The integrated trackpad means **one device** replaces keyboard + mouse in transit.

### Physical layout: pick your legends, set the keymap in software

This is the key thing to understand — and it means **you are not locked into AZERTY**
(or any layout):

- The **printed legends are cosmetic**. The actual keymap is decided in **software**:
  Android (*Settings → System → Languages → Physical keyboard*) and, if you want, inside
  the Debian VM with `setxkbmap fr` / `localectl set-x11-keymap fr` (or `us`, `de`, `gb`,
  `dvorak`, `colemak`, `bépo`…). You can even switch on the fly.
- So a **touch typist can use any model**, whatever is printed on the keys.
- If you **look at the keys**, buy the variant whose legends match your habit.

ProtoArc sells the XK01 TP in **QWERTY (US)**, **UK**, and **AZERTY (FR)**. Other
regional prints (e.g. German QWERTZ) aren't confirmed — check ProtoArc's regional store
or the local Amazon listing before buying. Whatever the print, the OS keymap above is
what actually types.

### Other foldable models

| Model | Trackpad | Notes |
|---|---|---|
| **ProtoArc XK01 TP** | ✅ large | The reference here — full-size keys, tri-fold |
| **ProtoArc XK01 Plus** | — | Backlit (good for dark cabins), no trackpad |
| **ProtoArc XKM01** | — (folding mouse) | Ships with a real folding mouse instead of a trackpad |
| **iClever BK06** | optional | Pocket-size tri-fold, near-full-size when open |
| **Samsers / SODI foldable** | ✅ | Cheaper tri-folds with touchpad; smaller keys |

Most of these ship **QWERTY-only**; remember the legends are cosmetic — set the keymap
in software regardless.

### Dynamic / reconfigurable mapping

- **In software (free, universal):** the practical "dynamic mapping" for pocketdesk is
  just the OS keymap — switch layouts per session, or even per-app, with no special
  hardware. This is what you'll actually use.
- **Programmable firmware (QMK/VIA):** lets you remap keys in the keyboard itself, but
  the **printed legends stay fixed**. No mainstream *foldable* QMK board exists today.
- **Display keycaps that re-label themselves:** the concept exists (e-ink/OLED under each
  key — see the table below), but nothing buyable, reliable **and folding** exists today,
  so it isn't a pocketdesk pick.

Coding-specific buying notes:

- Prefer layouts that keep **arrow keys + full-size Ctrl/Alt/Esc/Tab**. The XK01 does.
- A **rigid surface** is required — folding keyboards flex on laps.

### Tempting alternatives we don't recommend

Several "futuristic" input methods come up — all are real, all fail the
*actually-type-code* test:

| Method | Examples | Why not for pocketdesk |
|---|---|---|
| **Laser projection keyboard** | Celluon Epic, Serafim Keybo | Pairs fine over Bluetooth, but no tactile feedback or key travel; slow and typo-prone at ten fingers; needs a flat matte surface and washes out in bright light. |
| **Camera + AI "invisible" keyboard** | Samsung SelfieType (CES 2020) | The Pixel's camera could in theory track fingers on a bare table — but it never shipped as a product. |
| **Display keycaps (a screen per key)** | Art. Lebedev Optimus (OLED), Nemeio (e-ink) | The dream "dynamic legends" board — but Optimus is discontinued and Nemeio has been perennially delayed; neither folds. |
| **Screen under transparent keys** | Finalmouse Centerpiece | Dynamic visuals through the keycaps, but premium, gaming-focused, non-folding, repeatedly delayed. |
| **LCD-key macro pads** | Elgato Stream Deck, Mountain DisplayPad | Genuinely dynamic and shipping — but 6–32 keys: a shortcut pad, not something you type code on. |
| **Foldable phone screen as keyboard** | Pixel Fold / Galaxy Z Fold "flex" mode | Great as the *computer* (DP Alt Mode), but its glass inner screen as a keyboard fights the glasses: typing on glass needs your eyes *down*, the glasses put them *up*. No tactile feedback, hot under load, no trackpad. |

The honest takeaway: dynamic **legends** in hardware aren't a solved, buyable thing for a
typing keyboard — so pocketdesk gets its "dynamic layout" from the **software keymap**
above, on a physical folding board.

### If you type *looking at* the keys

The rejections above assume **blind touch typing** (eyes on the glasses). If you instead
type while looking at the keyboard — which the **see-through** glasses actually allow
(glance down to your hands, up to the virtual screen) — the calculus shifts for **one**
option:

- **Display / e-ink keycaps (Nemeio)** regain their whole point. Dynamic legends are
  *only* useful to someone who looks; for a blind typist they're invisible. And they keep
  **real keys** (travel + landmarks). For frequent layout switchers (QWERTY/AZERTY/Dvorak,
  per-app), it's the ideal — availability is the only catch. A **Stream Deck** complements
  it as a look-at-it shortcut pad.
- Flat surfaces (projection, glass/foldable) get *less bad* but still lack landmarks and
  travel.

**What about haptic feedback?** It helps less than you'd hope. A buzz/click on tap is
**confirmation** ("the key registered") — useful — but it doesn't restore the two things
blind/fast typing needs: **spatial landmarks** (finding keys, the F/J bumps, resting your
fingers) and **travel / activation feel**. A phone has *one* non-localized motor; the buzz
fires *after* contact. Localized fake-click haptics (Apple's Taptic Engine) work for a
**single button or a trackpad**, not a ten-finger keyboard — and on a bare projected table
there's nothing under your fingers to actuate at all. So haptics **narrows** the gap, it
doesn't close it. Remember a physical key already *is* haptic feedback (the switch) — which
is why a real folding keyboard beats any flat-surface-plus-haptics combo for sustained code.

> [!NOTE]
> **All input pairs in Android, not in the VM.** Pair the keyboard/trackpad/mouse under
> *Settings → Connected devices*, then set your layout (QWERTY, AZERTY, QWERTZ, Dvorak…)
> under *Settings → System → Languages → Physical keyboard*. Android forwards events into
> the Linux graphical surface — no `bluez` setup inside Debian. To override the keymap
> just for Linux apps, run `setxkbmap <layout>` in the VM session.
