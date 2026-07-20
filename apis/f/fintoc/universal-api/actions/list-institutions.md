# Fintoc: List Institutions

Retrieves institutions from Fintoc.

```
GET https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-institutions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-institutions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-institutions?${params}`, {
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
      "country": "string",
      "id": "string",
      "name": "Ava Chen",
      "object_name": "Ava Chen",
      "products": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object_name` | string |  |
| `products` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Fintoc API, this operation is `GET /v1/institutions` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-institutions.md) for the provider-specific parameters and requirements.

