# Speak Flatpak

Speak is a voice synthesis activity for the Sugar desktop.
Speak shows a face that will talk what is typed, within reason.

To know more refer: https://github.com/sugarlabs/speak

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.Speak.git
cd org.sugarlabs.Speak
flatpak -y --user install org.gnome.{Platform,Sdk}//44
flatpak-builder --user --force-clean --install build org.sugarlabs.Speak.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.Speak
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.Speak.json
```