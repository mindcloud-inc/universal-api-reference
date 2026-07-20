# Brevo: List Webhooks



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-webhooks?${params}`, {
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
      "webhooks": [
        {
          "channel": "string",
          "createdAt": "string",
          "description": "string",
          "events": [
            "string"
          ],
          "id": 1,
          "modifiedAt": "string",
          "type": "string",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `webhooks[].channel` | string |  |
| `webhooks[].createdAt` | string |  |
| `webhooks[].description` | string |  |
| `webhooks[].events[]` | string |  |
| `webhooks[].id` | number |  |
| `webhooks[].modifiedAt` | string |  |
| `webhooks[].type` | string |  |
| `webhooks[].url` | string |  |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/webhooks` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

