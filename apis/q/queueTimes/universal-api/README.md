# <img src="https://images.mindcloud.co/apps/icons/queue-times_1785420732089.png" alt="Queue Times logo" width="28" height="28"> Queue Times: Universal API

Read public theme-park group, park, and live queue-time data. Data provided by Queue-Times.com.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/queueTimes/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Park Queue Times](actions/get-park-queue-times.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queueTimes/latest/actions/get-park-queue-times?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Park

| Action | Method | Description |
| --- | --- | --- |
| [List Park Groups and Parks](actions/list-park-groups-and-parks.md) | GET |  |

### Ride Queue

| Action | Method | Description |
| --- | --- | --- |
| [Get Park Queue Times](actions/get-park-queue-times.md) | GET |  |

