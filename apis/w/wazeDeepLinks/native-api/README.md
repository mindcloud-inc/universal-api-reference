# Waze Deep Links: Native API Reference

A consolidated summary of Waze Deep Links's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/waze/deeplinks
- **API base URL:** `https://waze.com/ul`

## Authentication

### No Auth

No credentials required. Waze deep links are public URL constructions.

This API does not require request authentication.

[Official authentication documentation](https://developers.google.com/waze/deeplinks)

## API conventions

Responses from this API use plain text.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Navigate To Coordinates](actions/navigate-to-coordinates.md) | `GET https://waze.com/ul` | [docs](https://developers.google.com/waze/deeplinks) |
| [Navigate To Favorite](actions/navigate-to-favorite.md) | `GET https://waze.com/ul` | [docs](https://developers.google.com/waze/deeplinks) |
| [Search Address](actions/search-address.md) | `GET https://waze.com/ul` | [docs](https://developers.google.com/waze/deeplinks) |
| [Search And Navigate](actions/search-and-navigate.md) | `GET https://waze.com/ul` | [docs](https://developers.google.com/waze/deeplinks) |
| [Show Location On Map](actions/show-location-on-map.md) | `GET https://waze.com/ul` | [docs](https://developers.google.com/waze/deeplinks) |
| [Show Map At Zoom Level](actions/show-map-at-zoom-level.md) | `GET https://waze.com/ul` | [docs](https://developers.google.com/waze/deeplinks) |
