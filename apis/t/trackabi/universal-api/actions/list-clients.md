# Trackabi: List Clients

Retrieves clients from Trackabi.

```
GET https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/list-clients?${params}`, {
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
      "": [
        {
          "address": "string",
          "contactPerson": "string",
          "costHourlyRate": 1,
          "currency": "string",
          "email": "ava@example.com",
          "hourlyRate": 1,
          "id": 1,
          "logo": "string",
          "name": "Ava Chen",
          "notes": "string",
          "phone": "string",
          "shortName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].address` | string |  |
| `[].contactPerson` | string |  |
| `[].costHourlyRate` | number |  |
| `[].currency` | string |  |
| `[].email` | string |  |
| `[].hourlyRate` | number |  |
| `[].id` | number |  |
| `[].logo` | string |  |
| `[].name` | string |  |
| `[].notes` | string |  |
| `[].phone` | string |  |
| `[].shortName` | string |  |

## Native endpoint

Through the native Trackabi API, this operation is `GET /api/v1/clients` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

