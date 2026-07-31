# <img src="https://images.mindcloud.co/apps/icons/nasa-apod_1785426386813.png" alt="NASA APOD logo" width="28" height="28"> NASA APOD: Universal API

Browse astronomy pictures with NASA APOD metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nASAAPOD/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://apod.nasa.gov/apod/
- **Vendor API docs:** https://api.nasa.gov/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get APOD Date Range](actions/get-apod-date-range.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nASAAPOD/latest/actions/get-apod-date-range?connectionId=$CONNECTION_ID&start_date=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Astronomy Picture

| Action | Method | Description |
| --- | --- | --- |
| [Get Astronomy Picture of the Day](actions/get-astronomy-picture-of-the-day.md) | GET |  |

### Astronomy Pictures

| Action | Method | Description |
| --- | --- | --- |
| [Get APOD Date Range](actions/get-apod-date-range.md) | GET |  |
| [Get Random APODs](actions/get-random-apods.md) | GET |  |

