# Deepgram: Get Token Details

Retrieves API token details from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-token-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-token-details?${params}`, {
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
      "accessor": "string",
      "accessorGeneration": 1,
      "created": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "scopes": [
        "string"
      ],
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessor` | string |  |
| `accessorGeneration` | number |  |
| `created` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `scopes` | array<string> |  |
| `subject` | string |  |

## Native endpoint

Through the native Deepgram API, this operation is `GET /v1/auth/token` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-details.md) for the provider-specific parameters and requirements.

