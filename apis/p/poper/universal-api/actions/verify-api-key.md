# Poper: Verify API Key

Verifies a Poper API key and retrieves the account email.

```
GET https://connect.mindcloud.co/v1/universal/poper/latest/actions/verify-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poper/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poper/latest/actions/verify-api-key?${params}`, {
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
      "email": "ava@example.com",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address associated with the authenticated Poper API key. |
| `message` | string | Poper ping confirmation message. |

## Native endpoint

Through the native Poper API, this operation is `POST /ping` (base URL `https://api.poper.ai/general/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-api-key.md) for the provider-specific parameters and requirements.

