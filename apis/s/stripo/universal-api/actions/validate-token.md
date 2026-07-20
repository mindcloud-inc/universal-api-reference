# Stripo: Validate Token

Validates a Stripo API token.

```
GET https://connect.mindcloud.co/v1/universal/stripo/latest/actions/validate-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/validate-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripo/latest/actions/validate-token?${params}`, {
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
      "protocolVersion": "string",
      "valid": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `protocolVersion` | string | Stripo API protocol version. |
| `valid` | boolean | Whether the Stripo project API token is valid. |
| `version` | string | Stripo API version value when returned. |

## Native endpoint

Through the native Stripo API, this operation is `GET /validate` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-token.md) for the provider-specific parameters and requirements.

