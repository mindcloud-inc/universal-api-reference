# Sakari SMS: List Active Webhooks

Retrieves active webhooks from Sakari SMS.

```
GET https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-active-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-active-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-active-webhooks?${params}`, {
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
      "destination": "string",
      "eventTypes": [
        "string"
      ],
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `destination` | string |  |
| `eventTypes` | array<string> |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `GET /v1/accounts/:accountId/webhooks` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-webhooks.md) for the provider-specific parameters and requirements.

