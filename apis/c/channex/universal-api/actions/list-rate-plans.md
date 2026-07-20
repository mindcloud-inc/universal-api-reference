# Channex: List Rate Plans

Retrieves rate plans from your Channex account.

```
GET https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-rate-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-rate-plans?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-rate-plans?${params}`, {
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
          "attributes": {
            "currency": "string",
            "rate_mode": "string",
            "sell_mode": "string",
            "title": "string"
          },
          "id": "string",
          "relationships": {
            "property": {
              "data": {
                "id": "string"
              }
            },
            "room_type": {
              "data": {
                "id": "string"
              }
            }
          },
          "type": "string"
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
| `data[].attributes.currency` | string |  |
| `data[].attributes.rate_mode` | string |  |
| `data[].attributes.sell_mode` | string |  |
| `data[].attributes.title` | string |  |
| `data[].id` | string |  |
| `data[].relationships.property.data.id` | string |  |
| `data[].relationships.room_type.data.id` | string |  |
| `data[].type` | string |  |

## Native endpoint

Through the native Channex API, this operation is `GET /rate_plans` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-rate-plans.md) for the provider-specific parameters and requirements.

