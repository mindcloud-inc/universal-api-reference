# Syntage: List Credentials

Retrieves credentials from Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-credentials?${params}`, {
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
      "@id": "string",
      "@type": "string",
      "createdAt": "string",
      "id": "string",
      "rfc": "string",
      "status": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@id` | string |  |
| `@type` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `rfc` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Syntage API, this operation is `GET /credentials` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-credentials.md) for the provider-specific parameters and requirements.

