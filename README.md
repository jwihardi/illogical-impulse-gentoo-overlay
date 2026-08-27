# Illogical Impulse Gentoo Overlay

Gentoo overlay for [Illogical Impulse](https://github.com/end-4/dots-hyprland).

## Setup

Install `eselect-repository` if needed:

```bash
sudo emerge --update app-eselect/eselect-repository
```

Add the overlay:

```bash
sudo eselect repository add ii-dots git \
    https://github.com/jwihardi/illogical-impulse-gentoo-overlay.git
```

Sync repositories:

```bash
sudo emerge --sync
```

The overlay will be installed to:

```text
/var/db/repos/ii-dots
```

## Updating

Update normally with:

```bash
sudo emerge --sync
```

Or sync only this overlay:

```bash
sudo emaint sync -r ii-dots
```

## Removing

```bash
sudo eselect repository remove -f ii-dots
```
