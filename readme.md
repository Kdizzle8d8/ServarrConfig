Create a new network

```bash
docker network create movies --gateway 10.10.18.1 --subnet 10.10.18.0/24
```

**Jellyfin**
- Stream your networks and shows over the network
- **Port** : 8090

**Sonarr**
- TV show downloader. Search for shows in the WebUI and add them to your monitored list
- Any monitored episodes will be searched for and downlaoded, you can monitor singular episodes, whole seasons, or entire shows
- **Port** : 8989

**Radarr**
- Nearly identical to Radarr but for movies instead of shows
- **Port :7878

**Prowlarr**
- Torrent indexer manager for Radarr/Sonarr
- This will handle searching for torrents using "indexers" for each site (PiratesBay, 1337x, etc)
- **Port** :9696

**RDT Client**
- Download client for Radarr/Sonarr utiliting the real-debrid api.
- Real-Debrid is a service that has a large cache of torrents and allows you to put in a torrent/magnet and download the resulting file directly from them without having to worry about a VPN
- **Port** :6500

**Overseer**
- Request management service. Search for shows/movies in the webUI and Sonarr/Radarr will download them.
- Designed to be simpler and less fine grained, no options for individual torrent selection, but you can give other people access to it with the ability to make requests and have them eithier be manually aproved (to be sent to Radarr/Sonarr) or automatically approved, without needing to give them access to your sonarr/radarr
- **Port** :5055


