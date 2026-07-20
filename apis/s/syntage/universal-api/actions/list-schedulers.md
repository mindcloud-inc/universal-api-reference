# Syntage: List Schedulers

Retrieves schedulers from Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-schedulers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-schedulers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/list-schedulers?${params}`, {
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
      "isEnabled": true,
      "name": "Ava Chen",
      "rules": {},
      "tags": [
        {}
      ],
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
| `isEnabled` | boolean |  |
| `name` | string |  |
| `rules` | object |  |
| `tags` | array<object> |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Syntage API, this operation is `GET /schedulers` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-schedulers.md) for the provider-specific parameters and requirements.

