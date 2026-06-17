[![CodeFactor](https://www.codefactor.io/repository/github/UltraFeed/TorrServerEntware/badge)](https://www.codefactor.io/repository/github/UltraFeed/TorrServerEntware)

# TorrServer Entware Script

This script automatically manages TorrServer on Keenetic routers.

* Automatically starts TorrServer when the router boots up.
* Automatically updates TorrServer to the latest stable release on every startup.

## Requirements

* A Keenetic router with **Entware** installed.
* **curl** installed in your Entware environment (run `opkg update && opkg install curl` if missing).
* **Architecture:** ARM64 (configured by default for `TorrServer-linux-arm64`).

## One-Line Installation

Run the following command via SSH in your Entware environment to download the script, set the correct permissions, and trigger the initial setup and update:

```bash
curl -sL "https://raw.githubusercontent.com/UltraFeed/TorrServerEntware/main/S55torrserver" -o /opt/etc/init.d/S55torrserver && chmod +x /opt/etc/init.d/S55torrserver && /opt/etc/init.d/S55torrserver restart
```

> [!NOTE]
> Once installed, TorrServer will be available at http://<YOUR_ROUTER_IP>:8090/
