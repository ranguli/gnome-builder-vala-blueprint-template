# gnome-builder-vala-blueprint-template

This repository is the default Vala template project created by GNOME Builder, with 
the addition of support for [GNOME Blueprint](https://jwestman.pages.gitlab.gnome.org/blueprint-compiler/), 
implemented as outlined in the Blueprint [tutorial](https://jwestman.pages.gitlab.gnome.org/blueprint-compiler/setup.html).

## Usage

First ensure you have [GNOME Builder](https://flathub.org/apps/org.gnome.Builder) installed, 
as well as `meson` and `ninja`.

Install `blueprint-compiler`:

```bash
git clone https://gitlab.gnome.org/jwestman/blueprint-compiler
cd blueprint-compiler
meson _build
ninja -C _build install
```

Clone this repo and open it in GNOME Builder.

