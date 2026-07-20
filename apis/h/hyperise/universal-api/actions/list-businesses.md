# Hyperise: List Businesses

Retrieves businesses from Hyperise.

```
GET https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/list-businesses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/list-businesses?${params}`, {
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
      "data": [
        {
          "businessName": "Ava Chen",
          "createdAt": "string",
          "email": "ava@example.com",
          "id": 1,
          "updatedAt": "string",
          "website": "string"
        }
      ],
      "meta": {
        "currentPage": 1,
        "lastPage": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].businessName` | string |  |
| `data[].createdAt` | string |  |
| `data[].email` | string |  |
| `data[].id` | number |  |
| `data[].updatedAt` | string |  |
| `data[].website` | string |  |
| `meta.currentPage` | number |  |
| `meta.lastPage` | number |  |
| `meta.total` | number |  |

## Native endpoint

Through the native Hyperise API, this operation is `GET /businesses` (base URL `https://app.hyperise.io/api/v1/regular`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-businesses.md) for the provider-specific parameters and requirements.

