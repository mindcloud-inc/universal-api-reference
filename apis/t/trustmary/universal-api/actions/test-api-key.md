# Trustmary: Test API Key

Retrieves API key test results from Trustmary.

```
GET https://connect.mindcloud.co/v1/universal/trustmary/latest/actions/test-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trustmary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trustmary/latest/actions/test-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trustmary/latest/actions/test-api-key?${params}`, {
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
      "api_key_name": "Ava Chen",
      "message": "string",
      "organization_id": "string",
      "organization_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_key_name` | string | Trustmary API key label. |
| `message` | string | Trustmary API key validation result message. |
| `organization_id` | string | Trustmary organization identifier. |
| `organization_name` | string | Trustmary organization name. |

## Native endpoint

Through the native Trustmary API, this operation is `GET /test` (base URL `https://api.trustmary.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-api-key.md) for the provider-specific parameters and requirements.

