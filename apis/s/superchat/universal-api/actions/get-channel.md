# Superchat: Get Channel

Retrieves a channel from Superchat by ID.

```
GET https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-channel?connectionId=$CONNECTION_ID&channel_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-channel?${params}`, {
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
| `channel_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "inbox": {
        "id": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "name": "Ava Chen",
      "type": "string",
      "url": "https://example.com",
      "whats_app_business_account_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `inbox` | object |  |
| `inbox.id` | string |  |
| `inbox.name` | string |  |
| `inbox.url` | string |  |
| `name` | string |  |
| `type` | string |  |
| `url` | string |  |
| `whats_app_business_account_id` | string |  |

## Native endpoint

Through the native Superchat API, this operation is `GET /channels/{channel_id}` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.

