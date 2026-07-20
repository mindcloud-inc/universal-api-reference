# <img src="https://images.mindcloud.co/apps/icons/casting42_1774872607572.png" alt="Casting42 logo" width="28" height="28"> Casting42: Universal API

Manage casting talent records, media, and candidates.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/casting42/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://casting42.com
- **Vendor API docs:** https://documenter.getpostman.com/view/24607394/2s9YR6buRP

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Talents](actions/list-talents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/casting42/latest/actions/list-talents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Candidate

| Action | Method | Description |
| --- | --- | --- |
| [Get Candidate](actions/get-candidate.md) | GET | Retrieves a candidate from Casting42 by candidate tag. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | POST | Creates a Casting42 authentication token from your API key. |

### Talent

| Action | Method | Description |
| --- | --- | --- |
| [Create Talent](actions/create-talent.md) | POST | Creates a new talent in Casting42. |
| [List Talents](actions/list-talents.md) | GET | Retrieves all talent records from Casting42. |
| [Search Talents](actions/search-talents.md) | GET | Finds Casting42 talents by search criteria. |
| [Update Talent](actions/update-talent.md) | PUT | Updates an existing talent in Casting42. |

### Talent Audio

| Action | Method | Description |
| --- | --- | --- |
| [List Talent Audios](actions/list-talent-audios.md) | GET | Retrieves audio files for a Casting42 talent. |

### Talent Field

| Action | Method | Description |
| --- | --- | --- |
| [List Talent Fields](actions/list-talent-fields.md) | GET | Retrieves available talent fields from Casting42. |

### Talent Media

| Action | Method | Description |
| --- | --- | --- |
| [Search Talent Media](actions/search-talent-media.md) | GET | Finds talent media in Casting42 by talent tag. |

### Talent Photo

| Action | Method | Description |
| --- | --- | --- |
| [List Talent Photos](actions/list-talent-photos.md) | GET | Retrieves photos for a Casting42 talent. |
| [Optimize Talent Photos](actions/optimize-talent-photos.md) | PUT | Optimizes photos for a Casting42 talent. |
| [Search Talent Photos](actions/search-talent-photos.md) | GET | Finds talent photos in Casting42 by talent tag. |
| [Upload Talent Photo](actions/upload-talent-photo.md) | POST | Uploads a photo for a Casting42 talent. |

