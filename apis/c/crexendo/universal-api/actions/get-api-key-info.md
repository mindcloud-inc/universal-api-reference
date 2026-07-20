# Crexendo: Get API Key Info

Retrieves API key info from Crexendo.

```
GET https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/get-api-key-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crexendo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/get-api-key-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/get-api-key-info?${params}`, {
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
      "can-create-keys": "string",
      "created-datetime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "key-id": "string",
      "readonly": "string",
      "reseller": "string",
      "user-scope": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can-create-keys` | string |  |
| `created-datetime` | date |  |
| `description` | string |  |
| `key-id` | string |  |
| `readonly` | string |  |
| `reseller` | string |  |
| `user-scope` | string |  |

## Native endpoint

Through the native Crexendo API, this operation is `GET /apikeys/~` (base URL `https://ns-api.com/ns-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-key-info.md) for the provider-specific parameters and requirements.

