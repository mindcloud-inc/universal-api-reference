# vionvi CRM: List Catalog Items

Retrieves catalog items from vionvi CRM.

```
GET https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/list-catalog-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vionvi CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/list-catalog-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/list-catalog-items?${params}`, {
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
      "dtCreate": 1,
      "dtUpdate": 1,
      "id": 1,
      "isActive": 1,
      "name": "Ava Chen",
      "price": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dtCreate` | number |  |
| `dtUpdate` | number |  |
| `id` | number |  |
| `isActive` | number |  |
| `name` | string |  |
| `price` | number |  |

## Native endpoint

Through the native vionvi CRM API, this operation is `GET /catalog` (base URL `https://280-crm-api.vionvi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-catalog-items.md) for the provider-specific parameters and requirements.

