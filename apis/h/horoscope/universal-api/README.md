# <img src="https://images.mindcloud.co/apps/icons/horoscope_1785360070096.png" alt="Horoscope logo" width="28" height="28"> Horoscope: Universal API

Get daily, weekly, and monthly horoscope readings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/horoscope/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://freehoroscopeapi.com/
- **Vendor API docs:** https://freehoroscopeapi.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Daily Horoscope](actions/get-daily-horoscope.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/horoscope/latest/actions/get-daily-horoscope?connectionId=$CONNECTION_ID&sign=aquarius" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Horoscope

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Horoscope](actions/get-daily-horoscope.md) | GET |  |
| [Get Monthly Horoscope](actions/get-monthly-horoscope.md) | GET |  |
| [Get Weekly Horoscope](actions/get-weekly-horoscope.md) | GET |  |

