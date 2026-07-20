# Ordoro: Get API Key by ID

Retrieves an API key from Ordoro by ID.

```
GET https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-api-key-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ordoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-api-key-by-id?connectionId=$CONNECTION_ID&apiKeyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apiKeyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-api-key-by-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiKeyId` | string | yes | The Ordoro API key ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Ordoro API, this operation is `GET /api_key/{api_key_id}/` (base URL `https://api.ordoro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-key-by-id.md) for the provider-specific parameters and requirements.

