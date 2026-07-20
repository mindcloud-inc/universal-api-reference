# xMatters: Get sites

Retrieves sites from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-sites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-sites?${params}`, {
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
      "count": 1,
      "data": [
        {
          "address1": "string",
          "address2": "string",
          "city": "string",
          "country": "string",
          "externallyOwned": true,
          "id": "string",
          "language": "string",
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen",
          "postalCode": "string",
          "state": "string",
          "status": "string",
          "timezone": "string"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].address1` | string |  |
| `data[].address2` | string |  |
| `data[].city` | string |  |
| `data[].country` | string |  |
| `data[].externallyOwned` | boolean |  |
| `data[].id` | string |  |
| `data[].language` | string |  |
| `data[].links.self` | string |  |
| `data[].name` | string |  |
| `data[].postalCode` | string |  |
| `data[].state` | string |  |
| `data[].status` | string |  |
| `data[].timezone` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET sites` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-sites.md) for the provider-specific parameters and requirements.

