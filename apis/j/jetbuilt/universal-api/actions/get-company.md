# Jetbuilt: Get Company



```
GET https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-company?${params}`, {
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
      "createdAt": "string",
      "id": 1,
      "locations": [
        {
          "address": "string",
          "city": "string",
          "country": "string",
          "createdAt": "string",
          "id": 1,
          "name": "Ava Chen",
          "productDatabaseId": 1,
          "state": "string",
          "timeZone": "string",
          "updatedAt": "string",
          "zipcode": "string"
        }
      ],
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | number |  |
| `locations` | array<object> |  |
| `locations[].address` | string |  |
| `locations[].city` | string |  |
| `locations[].country` | string |  |
| `locations[].createdAt` | string |  |
| `locations[].id` | number |  |
| `locations[].name` | string |  |
| `locations[].productDatabaseId` | number |  |
| `locations[].state` | string |  |
| `locations[].timeZone` | string |  |
| `locations[].updatedAt` | string |  |
| `locations[].zipcode` | string |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Jetbuilt API, this operation is `GET company` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

