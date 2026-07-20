# IronWiFi: List Tariff Groups

Retrieves tariff groups from IronWiFi.

```
GET https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/list-tariff-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IronWiFi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/list-tariff-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/list-tariff-groups?${params}`, {
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
      "embedded": {},
      "page": 1,
      "pageCount": 1,
      "pageSize": 1,
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `embedded` | object | HAL embedded collection payload returned by IronWiFi for this resource list. |
| `page` | number | Current page number returned by IronWiFi. |
| `pageCount` | number | Total number of pages available for this result set. |
| `pageSize` | number | Number of records included per page. |
| `totalItems` | number | Total number of records available across all pages. |

## Native endpoint

Through the native IronWiFi API, this operation is `GET /tariff-groups` (base URL `https://console.ironwifi.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tariff-groups.md) for the provider-specific parameters and requirements.

