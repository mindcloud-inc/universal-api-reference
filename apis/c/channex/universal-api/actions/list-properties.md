# Channex: List Properties

Retrieves properties from your Channex account.

```
GET https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-properties?${params}`, {
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
            "city": "string",
            "country": "string",
            "currency": "string",
            "is_active": true,
            "title": "string"
          },
          "id": "string",
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
| `data[].attributes.city` | string |  |
| `data[].attributes.country` | string |  |
| `data[].attributes.currency` | string |  |
| `data[].attributes.is_active` | boolean |  |
| `data[].attributes.title` | string |  |
| `data[].id` | string |  |
| `data[].type` | string |  |

## Native endpoint

Through the native Channex API, this operation is `GET /properties` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-properties.md) for the provider-specific parameters and requirements.

