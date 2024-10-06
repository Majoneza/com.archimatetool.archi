# Archi

The Open Source modelling toolkit for creating ArchiMate models and sketches.

This repo hosts the flatpak wrapper for [Archi](https://www.archimatetool.com/).

## Looking for a newer version?

1) Clone the git repo and navigate into it

```bash
git clone https://github.com/Majoneza/com.archimatetool.archi archi
cd archi
```

2) Update `com.archimatetool.archi.json` to the desired Archi version, for example going from version 4.9.1 to 5.4.2:

```diff
"sources": [
    {
        "type": "archive",
-       "url": "https://www.archimatetool.com/downloads/archi/5.2.0/Archi-Linux64-5.2.0.tgz",
+       "url": "https://www.archimatetool.com/downloads/archi/5.4.2/Archi-Linux64-5.4.2.tgz",
-       "sha256": "b865b85a5dc4ef5642816ccf1e4997bff3e5b9e80317c0bae05510ec2e7f4830",
+       "sha256": "19c568b9a242f79e4b691b702573ad9271278c713543335ea164aa00f17dcc61",
        "strip-components": 0
    },
    {
```

You can get the new sha256 by running `sha256sum Archi-Linux64-5.4.2.tgz`.

3) Build and install the flatpak (requires flatpak-builder)

```bash
flatpak-builder ./build com.archimatetool.archi.json --install --user
```

4) Now you should be able to run the app

```bash
flatpak run com.archimatetool.archi
```

You are free to delete the cloned repository or keep it for future updates.
