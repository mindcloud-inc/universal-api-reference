# Ubiqod by Skiply: Get Tracker



```
GET https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/get-tracker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubiqod by Skiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/get-tracker?connectionId=$CONNECTION_ID&trackerSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackerSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/get-tracker?${params}`, {
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
| `trackerSlug` | string | yes | Tracker slug. |

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

Through the native Ubiqod by Skiply API, this operation is `GET /trackers/:trackerSlug` (base URL `https://api.ubiqod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracker.md) for the provider-specific parameters and requirements.

