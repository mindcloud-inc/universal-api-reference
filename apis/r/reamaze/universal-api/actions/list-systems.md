# Reamaze: List Systems



```
GET https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-systems
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-systems?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-systems?${params}`, {
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
      "accountId": 1,
      "activeIncidents": [
        {}
      ],
      "brandId": 1,
      "createdAt": "string",
      "id": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `activeIncidents` | array<object> |  |
| `brandId` | number |  |
| `createdAt` | string |  |
| `id` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Reamaze API, this operation is `GET /systems` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-systems.md) for the provider-specific parameters and requirements.

