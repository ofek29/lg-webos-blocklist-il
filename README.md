# LG webOS blocklist · Israel / EIC

Reduce LG home-screen promotions and telemetry in Israel / EIC. Keep your existing lists for broader coverage.

Based on real DNS traffic from an LG webOS TV in Israel, expanded with DNS-verified regional endpoints.

## Choose your level

| List | Use it for |
| --- | --- |
| **[Default](lg-israel.txt)** | Start here: lower-risk ads, recommendations, and telemetry. |
| **[Aggressive add-on](lg-israel-aggressive.txt)** | Extra platform and ThinQ blocking. Add alongside the default. |

Hosts format for AdAway / AdGuard Home: [default](lg-israel-hosts.txt) · [aggressive](lg-israel-aggressive-hosts.txt). Choose one format per level.

**Aggressive blocking may affect the home screen, app store, sign-in, guide data, time sync, ThinQ, and other LG devices.**

Syntax checks passed. Real-TV blocking tests are pending.

## Install in Pi-hole v6

1. Open the **Default** file above, select **Raw**, and copy its URL.
2. Add the URL under **Lists** as a blocking list.
3. Run **Tools → Update Gravity**, then restart the TV.

For more blocking, add the **Aggressive add-on** the same way.

### Optional regex rules

[regex.txt](regex.txt) covers service families across regions. Add selected patterns under **Domains** as **regex deny** entries, not under Lists. Copy patterns without comments. The file explains each risk level.

## If a feature stops working

Disable the aggressive list and optional regex rules, update Gravity, and restart the TV. Disable the default too if needed. Use **Query Log** to identify domains to allow. The four update/content hosts documented in the lists stay inactive here, but other lists can still block them.

References: [Perflyst](https://github.com/Perflyst/PiHoleBlocklist) · [HaGeZi's LG list](https://github.com/hagezi/dns-blocklists/blob/main/wildcard/native.lgwebos.txt) · [Gamers Nexus](https://www.youtube.com/watch?v=6IFVTcM28KA) · [Wendell's guide](https://forum.level1techs.com/t/lg-tv-block-mini-how-to/255178).
