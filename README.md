This plugin enables users to display the proxy information, such as country, region, city, proxy type, and security threat derived from the IP addresses.

Instructions
============

1. Install **Geo::IP2Proxy** libraries from CPAN.

    ```
    cpan > install Geo::IP2Proxy
    ```

    

2. Upload **ip2proxy.pm** to `/usr/share/awstats/plugins`.

3. Download the free [IP2Proxy PX9 LITE](https://lite.ip2location.com/database/px9-ip-proxytype-country-region-city-isp-domain-usagetype-asn-lastseen-threat) database or commercial [IP2Proxy PX9](https://www.ip2location.com/database/px9-ip-proxytype-country-region-city-isp-domain-usagetype-asn-lastseen-threat) database.

4. Decompress the package and upload the BIN file to `/usr/share/ip2proxy` directory.

5. Open `/etc/awstats/awstats.conf` and insert following line:

        LoadPlugin="ip2proxy /usr/share/ip2proxy/IP2PROXY-LITE-PX9.BIN"

    **Note: ** Make sure the path to IP2Proxy database file is correct.

6. Disable any Maxmind GeoIP plugin or IP2Location Geolocation plugin as AWStats hook can only access by one plugin per time.

7. View the information by accessing "Countries" or "Hosts" from the left menu.

    
Dependencies
============
It's recommended to use IP2Proxy PX9 which includes country, region, city, proxy type, and security threat information.
* IP2Proxy LITE (Free): https://lite.ip2location.com
* IP2Proxy Commercial (Comprehensive): https://www.ip2location.com


IPv4 BIN vs IPv6 BIN
====================
Use the IPv4 BIN file if you just need to query IPv4 addresses.

Use the IPv6 BIN file if you need to query BOTH IPv4 and IPv6 addresses.

