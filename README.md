# Illogical Impulse Gentoo Overlay

Gentoo overlay for [Illogical Impulse](https://github.com/end-4/dots-hyprland).

## Setup

```bash
# Install eselect-repository
sudo emerge --update app-eselect/eselect-repository

# Add the overlay
sudo eselect repository add ii-dots git \
    https://github.com/jwihardi/illogical-impulse-gentoo-overlay.git

# Sync only this overlay
sudo emaint sync -r ii-dots

# Alternatively, sync all configured repositories
# sudo emerge --sync
```

The overlay is installed to `/var/db/repos/ii-dots`.

## Updating

Use `sudo emerge --sync` to sync all configured repositories, or `sudo emaint sync -r ii-dots` to update only this overlay.

## Removing

Remove the overlay with `sudo eselect repository remove -f ii-dots`.
