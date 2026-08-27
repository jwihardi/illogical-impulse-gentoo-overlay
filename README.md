# Illogical Impulse Gentoo Overlay

Gentoo overlay for [Illogical Impulse](https://github.com/end-4/dots-hyprland). Use this overlay to update through Portage instead of cloning the end-4 repo each time.

## Pre-setup

If you previously used Gentoo support from [end-4/dots-hyprland](https://github.com/end-4/dots-hyprland), remove the old `ii-dots` repo first.

You don't need to uninstall the Illogical Impulse packages.

Older installs may have created `ii-dots` with `eselect-repository`:

```bash
sudo eselect repository remove -f ii-dots
```

If that says the repo is not registered, skip it.

Then remove any old local repo files:

```bash
sudo rm -f -- /etc/portage/repos.conf/ii-dots.conf
sudo rm -rf -- /var/db/repos/ii-dots
```

Keep your existing `package.use` and `package.accept_keywords` files.

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
