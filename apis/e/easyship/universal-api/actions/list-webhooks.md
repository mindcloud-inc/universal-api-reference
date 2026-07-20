# Easyship: List Webhooks

Retrieves a list of webhooks from Easyship.

```
GET https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-webhooks?${params}`, {
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
      "configuration": {},
      "createdAt": "string",
      "endpoint": "string",
      "eventTypes": [
        "string"
      ],
      "id": "string",
      "secretToken": "string",
      "state": "string",
      "updatedAt": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | object |  |
| `createdAt` | string |  |
| `endpoint` | string |  |
| `eventTypes` | array<string> |  |
| `id` | string |  |
| `secretToken` | string |  |
| `state` | string |  |
| `updatedAt` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Easyship API, this operation is `GET /webhooks` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

