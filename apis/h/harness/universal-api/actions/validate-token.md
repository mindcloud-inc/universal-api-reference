# Harness: Validate Token

Validates an access token in Harness.

```
GET https://connect.mindcloud.co/v1/universal/harness/latest/actions/validate-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harness/latest/actions/validate-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harness/latest/actions/validate-token?${params}`, {
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
      "principalName": "Ava Chen",
      "tokenType": "string",
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `principalName` | string |  |
| `tokenType` | string |  |
| `valid` | boolean |  |

## Native endpoint

Through the native Harness API, this operation is `POST /ng/api/token/validate` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-token.md) for the provider-specific parameters and requirements.

