# ESRI: Native API Reference

A consolidated summary of ESRI's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://developers.arcgis.com/rest/
- **API base URL:** `https://www.arcgis.com/sharing/rest`

## Authentication

### API Key

ArcGIS API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.arcgis.com/documentation/security-and-authentication/api-key-authentication/)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Portal Self](actions/portal-self.md) | `GET https://www.arcgis.com/sharing/rest/portals/self` | [docs](https://developers.arcgis.com/rest/users-groups-and-items/portal-self/) |
