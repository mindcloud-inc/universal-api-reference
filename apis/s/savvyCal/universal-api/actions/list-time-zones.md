# SavvyCal: List Time Zones



```
GET https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-time-zones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SavvyCal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-time-zones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/savvyCal/latest/actions/list-time-zones?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instant` | date | no |  |
| `includeLegacy` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abbreviation": "string",
      "aliases": [
        "string"
      ],
      "canonical": true,
      "dst": true,
      "formattedOffset": "string",
      "genericLongName": "Ava Chen",
      "golden": true,
      "id": "string",
      "legacy": true,
      "longName": "Ava Chen",
      "metazone": {
        "exemplarCity": "string",
        "long": {
          "current": "string"
        },
        "name": "Ava Chen",
        "short": {
          "current": "string"
        }
      },
      "offset": 1,
      "offsetStd": 1,
      "offsetUtc": 1,
      "period": {
        "from": "2026-05-07T12:00:00.000Z",
        "until": "2026-05-07T12:00:00.000Z"
      },
      "windowsZone": {
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abbreviation` | string | Time zone abbreviation. |
| `aliases[]` | string | Alternative identifiers for the time zone. |
| `canonical` | boolean | Whether the time zone is canonical. |
| `dst` | boolean | Whether daylight saving time is active. |
| `formattedOffset` | string | Human-readable UTC offset. |
| `genericLongName` | string | Generic long display name for the time zone. |
| `golden` | boolean | Whether the time zone is a CLDR golden zone. |
| `id` | string | IANA time zone identifier. |
| `legacy` | boolean | Whether the time zone is legacy. |
| `longName` | string | Long display name for the time zone. |
| `metazone.exemplarCity` | string | Metazone exemplar city. |
| `metazone.long.current` | string | Current long metazone label. |
| `metazone.name` | string | Metazone identifier. |
| `metazone.short.current` | string | Current short metazone label. |
| `offset` | number | Current offset from UTC in seconds. |
| `offsetStd` | number | Offset from standard time in seconds. |
| `offsetUtc` | number | Standard offset from UTC in seconds. |
| `period.from` | date | Start of the current period. |
| `period.until` | date | End of the current period. |
| `windowsZone.name` | string | Mapped Windows time zone name. |

## Native endpoint

Through the native SavvyCal API, this operation is `GET /v1/time_zones` (base URL `https://api.savvycal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-zones.md) for the provider-specific parameters and requirements.

