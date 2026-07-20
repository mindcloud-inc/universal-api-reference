# <img src="https://images.mindcloud.co/apps/icons/nasa-logo-large_1776350566506.jpeg" alt="APOD logo" width="28" height="28"> APOD: Universal API

Retrieve NASA astronomy images and metadata

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aPOD/latest
- **Category:** Website & App Building / CMS
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://apod.nasa.gov/apod/astropix.html
- **Vendor API docs:** https://api.nasa.gov/#apod

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Today's Astronomy Picture](actions/get-todays-astronomy-picture.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPOD/latest/actions/get-todays-astronomy-picture?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Astronomy Picture

| Action | Method | Description |
| --- | --- | --- |
| [Get Astronomy Picture by Date](actions/get-astronomy-picture-by-date.md) | GET | Retrieves an APOD entry from NASA by date. |
| [Get Random Astronomy Pictures](actions/get-random-astronomy-pictures.md) | GET | Retrieves random APOD entries from NASA. |
| [Get Today's Astronomy Picture](actions/get-todays-astronomy-picture.md) | GET | Retrieves today's APOD entry from NASA. |
| [List Astronomy Pictures by Date Range](actions/list-astronomy-pictures-by-date-range.md) | GET | Retrieves APOD entries from NASA by date range. |

