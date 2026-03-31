# deck-plymouth-theme
Deck Plymouth (Steam Deck style)

# Deck Plymouth (Steam Deck Style)

Steam Deck–style boot splash theme for Bazzite.

## Requirements

* Bazzite (rpm-ostree based system)

---

## Installation

### 1. Download the RPM

Download:

```
deck-plymouth-1.0-1.fc42.noarch.rpm
```

---

### 2. Install required plugin (IMPORTANT)

This theme requires the Plymouth script plugin:

```bash
sudo rpm-ostree install plymouth-plugin-script
```

---

### 3. Install the theme (open terminal/konsole in the folder .rpm is located)

```bash
sudo rpm-ostree install ./deck-plymouth-1.0-1.fc42.noarch.rpm
```

---

### 4. Set the theme

```bash
sudo plymouth-set-default-theme deck
```

---

### 5. Enable initramfs updates (only needed once)

```bash
sudo rpm-ostree initramfs --enable
```

---

### 6. Reboot

```bash
systemctl reboot
```

---

## Revert to default

```bash
sudo plymouth-set-default-theme bgrt
systemctl reboot
```

---

## Notes

* If the plugin is missing, you may see a black screen.
* The theme will fully apply after reboot.
* Works on Bazzite and other rpm-ostree systems.
