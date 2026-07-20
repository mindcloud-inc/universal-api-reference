# TikTok Conversions: Delete Offline Event Set

Deletes an existing Offline Event set from TikTok Conversions.

```
DELETE https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/delete-offline-event-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Conversions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/delete-offline-event-set?connectionId=$CONNECTION_ID&advertiser_id=string&event_set_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "advertiser_id": "string",
  "event_set_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/delete-offline-event-set?${params}`, {
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
| `advertiser_id` | string | yes |  |
| `event_set_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "message": "string",
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `message` | string |  |
| `request_id` | string |  |

## Native endpoint

Through the native TikTok Conversions API, this operation is `POST /open_api/v1.3/offline/delete/` (base URL `https://business-api.tiktok.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-offline-event-set.md) for the provider-specific parameters and requirements.

