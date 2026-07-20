# Casting42: Native API Reference

A consolidated summary of Casting42's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/24607394/2s9YR6buRP
- **API base URL:** `https://casting42.com`

## Authentication

### API Key Bootstrap 2

Bootstrap auth with persisted auth action.

### Credentials

- **API Key:** `apiKey` · required · Provider-native Casting42 API key copied from Settings > API.

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documenter.getpostman.com/view/24607394/2s9YR6buRP)

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST /api/v2/auth` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
| [Create Talent](actions/create-talent.md) | `POST /api/v2/talents` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
| [Get Candidate](actions/get-candidate.md) | `GET /api/v2/candidates/{{candidateTag}}` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
| [List Talent Audios](actions/list-talent-audios.md) | `GET /api/v2/talents/audios/{{talentTag}}` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
| [List Talent Fields](actions/list-talent-fields.md) | `GET /api/v2/settings/fields` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
| [List Talent Photos](actions/list-talent-photos.md) | `GET /api/v2/talents/photos/{{talentTag}}/medium` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
| [List Talents](actions/list-talents.md) | `GET /api/v2/talents` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
| [Optimize Talent Photos](actions/optimize-talent-photos.md) | `GET /api/v2/talents/optimize-photos-of-talent/{{talentTag}}` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
| [Search Talent Media](actions/search-talent-media.md) | `POST /api/v2/talents/media/find` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
| [Search Talent Photos](actions/search-talent-photos.md) | `POST /api/v2/talents/photos/find` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
| [Search Talents](actions/search-talents.md) | `POST /api/v2/talents/find` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
| [Update Talent](actions/update-talent.md) | `PATCH /api/v2/talents/update` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
| [Upload Talent Photo](actions/upload-talent-photo.md) | `POST /talents/upload-photo` | [docs](https://documenter.getpostman.com/view/24607394/2s9YR6buRP) |
