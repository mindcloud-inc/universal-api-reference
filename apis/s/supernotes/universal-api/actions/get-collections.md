# Supernotes: Get Collections

Retrieves your saved collections from Supernotes.

```
GET https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supernotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-collections?${params}`, {
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
      "createdWhen": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "modifiedWhen": "2026-05-07T12:00:00.000Z",
      "order": "string",
      "spec": {},
      "view": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdWhen` | date |  |
| `id` | string |  |
| `modifiedWhen` | date |  |
| `order` | string |  |
| `spec` | object |  |
| `view` | object |  |

## Native endpoint

Through the native Supernotes API, this operation is `GET /collections` (base URL `https://api.supernotes.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collections.md) for the provider-specific parameters and requirements.

