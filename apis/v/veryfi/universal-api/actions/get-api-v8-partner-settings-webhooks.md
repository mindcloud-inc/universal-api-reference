# Veryfi: Get webhooks

Retrieves webhooks from Veryfi.

```
GET https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-settings-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-settings-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-settings-webhooks?${params}`, {
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
      "confirmed": [
        {}
      ],
      "pending": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmed` | array<object> |  |
| `pending` | array<object> |  |

## Native endpoint

Through the native Veryfi API, this operation is `GET /api/v8/partner/settings/webhooks` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-v8-partner-settings-webhooks.md) for the provider-specific parameters and requirements.

