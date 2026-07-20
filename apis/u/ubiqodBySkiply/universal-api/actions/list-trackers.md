# Ubiqod by Skiply: List Trackers



```
GET https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-trackers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubiqod by Skiply `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-trackers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-trackers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "dispatches": [
        "string"
      ],
      "enabled": true,
      "expiration_date": "2026-05-07T12:00:00.000Z",
      "externalReferences": {},
      "id": "string",
      "interface_id": "string",
      "label": "string",
      "last_data": "2026-05-07T12:00:00.000Z",
      "last_seen": "2026-05-07T12:00:00.000Z",
      "site_id": "string",
      "site_label": "string",
      "site_latitude": 1,
      "site_longitude": 1,
      "slug": "string",
      "subtype": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dispatches` | array<string> | Dispatch IDs attached to the tracker. |
| `enabled` | boolean | Whether the tracker is enabled. |
| `expiration_date` | date | Expiration date. |
| `externalReferences` | object | External reference map. |
| `id` | string | Tracker ID. |
| `interface_id` | string | Interface ID. |
| `label` | string | Tracker label. |
| `last_data` | date | Last data timestamp. |
| `last_seen` | date | Last seen timestamp. |
| `site_id` | string | Site ID. |
| `site_label` | string | Site label. |
| `site_latitude` | number | Site latitude. |
| `site_longitude` | number | Site longitude. |
| `slug` | string | Tracker slug. |
| `subtype` | string | Tracker subtype. |
| `type` | string | Tracker type. |

## Native endpoint

Through the native Ubiqod by Skiply API, this operation is `GET /trackers/` (base URL `https://api.ubiqod.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-trackers.md) for the provider-specific parameters and requirements.

