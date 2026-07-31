# <img src="https://images.mindcloud.co/apps/icons/mcu-countdown_1785426359979.png" alt="MCU Countdown logo" width="28" height="28"> MCU Countdown: Universal API

Retrieve the next MCU production and its following production from the public MCU Countdown API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mCUCountdown/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Next MCU Production](actions/get-next-mcu-production.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mCUCountdown/latest/actions/get-next-mcu-production?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Mcu Production

| Action | Method | Description |
| --- | --- | --- |
| [Get Next MCU Production](actions/get-next-mcu-production.md) | GET |  |

