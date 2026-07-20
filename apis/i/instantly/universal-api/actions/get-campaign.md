# Instantly: Get Campaign

Retrieves a campaign from Instantly.

```
GET https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-campaign?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-campaign?${params}`, {
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
| `id` | string | yes | Campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_schedule": {},
      "id": "string",
      "name": "Ava Chen",
      "open_tracking": true,
      "organization": "string",
      "status": 1,
      "timestamp_created": "2026-05-07T12:00:00.000Z",
      "timestamp_updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_schedule` | object |  |
| `id` | string |  |
| `name` | string |  |
| `open_tracking` | boolean |  |
| `organization` | string |  |
| `status` | number |  |
| `timestamp_created` | date |  |
| `timestamp_updated` | date |  |

## Native endpoint

Through the native Instantly API, this operation is `GET /api/v2/campaigns/:id` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

