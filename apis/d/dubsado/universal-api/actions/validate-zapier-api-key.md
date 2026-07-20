# Dubsado: Validate Zapier API Key

Validates a Zapier API key in Dubsado.

```
GET https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/validate-zapier-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dubsado `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/validate-zapier-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/validate-zapier-api-key?${params}`, {
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
      "brand": "string",
      "code": "string",
      "description": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | string |  |
| `code` | string |  |
| `description` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Dubsado API, this operation is `GET /zapier/key` (base URL `https://app.dubsado.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-zapier-api-key.md) for the provider-specific parameters and requirements.

