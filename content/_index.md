---
title: "pocketdesk"
layout: hextra-home
toc: false
---

{{< hextra/hero-badge >}}
  <div class="hx:w-2 hx:h-2 hx:rounded-full hx:bg-primary-400"></div>
  Pixel 10 Pro XL today · 11 Pro XL tomorrow
{{< /hextra/hero-badge >}}

<div class="hx:mt-6 hx:mb-6">
{{< hextra/hero-headline >}}
  Your phone is the&nbsp;workstation
{{< /hextra/hero-headline >}}
</div>

<div class="hx:mb-12">
{{< hextra/hero-subtitle >}}
  Code in VS&nbsp;Code on Linux running on a Pixel, projected onto AR glasses,&nbsp;<br class="hx:hidden hx:sm:block" />driven by a folding keyboard. A real desktop — in your pocket. No laptop.
{{< /hextra/hero-subtitle >}}
</div>

<div class="hx:mb-6">
{{< hextra/hero-button text="Get started" link="overview/" >}}
</div>

<div class="hx:mt-6"></div>

{{< hextra/feature-grid >}}
  {{< hextra/feature-card
    title="Phone is the computer"
    subtitle="Android's Linux Terminal runs a full Debian VM (AVF/KVM). On Pixel it includes GPU-accelerated GUI apps — a real VS Code window."
  >}}
  {{< hextra/feature-card
    title="Glasses are the screen"
    subtitle="USB-C DisplayPort drives the AR glasses as a 1200p wearable monitor — Viture Beast / Luma Ultra or XREAL 1S."
  >}}
  {{< hextra/feature-card
    title="Folding keyboard"
    subtitle="A tri-fold Bluetooth keyboard with trackpad pairs in Android and is forwarded into the VM. One device replaces keyboard + mouse."
  >}}
  {{< hextra/feature-card
    title="Linux + VS Code"
    subtitle="labwc (Wayland) + VS Code natively, or code-server in the browser as a rock-solid fallback. Tile windows for multi-pane."
  >}}
{{< /hextra/feature-grid >}}

## Start here

{{< cards >}}
  {{< card link="overview/" title="Overview" subtitle="What this is and why it works" >}}
  {{< card link="hardware/" title="Hardware" subtitle="Phone, glasses, keyboard" >}}
  {{< card link="multi-screen/" title="Multi-screen (AR)" subtitle="What's real, and where it lives" >}}
  {{< card link="linux-terminal/" title="Linux Terminal" subtitle="Enable the Debian VM" >}}
  {{< card link="desktop-wayland/" title="Wayland desktop" subtitle="labwc + input" >}}
  {{< card link="vscode/" title="VS Code" subtitle="Native GUI install" >}}
  {{< card link="code-server/" title="code-server" subtitle="The reliable fallback" >}}
  {{< card link="troubleshooting/" title="Troubleshooting" subtitle="When things go sideways" >}}
{{< /cards >}}

## The stack at a glance

![pocketdesk stack: Pixel host → AR display, Bluetooth keyboard, Android Linux Terminal → labwc + VS Code / code-server](/images/stack.svg)

> [!NOTE]
> This is a community knowledge base, not affiliated with Google, Viture, or ProtoArc.
> Pre-release device specs are leaks and must be re-confirmed at launch.
