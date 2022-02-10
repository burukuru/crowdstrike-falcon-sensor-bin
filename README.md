# crowdstrike-falcon-sensor-bin

Arch Linux `PKGBUILD` for CrowdStrike Falcon Sensor.

Uses Ubuntu DEB package for source files which can be downloaded from the CrowdStrike website to match the `pkgver` in the `PKGBUILD`, putting it in this directory before running `makepkg`.

The service will fail on first startup and you will need to link the agent and restart:

```
sudo /opt/CrowdStrike/falconctl -s --cid=<CID>
sudo systemctl restart falcon-sensor
```
