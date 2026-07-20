# Mailchimp: List E-commerce Stores

Retrieves e-commerce stores from Mailchimp.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-e-commerce-stores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-e-commerce-stores?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-e-commerce-stores?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | A comma-separated list of fields to return. Accepts multiple values as an array. Example: `id,name`. |
| `excludeFields` | string | no | A comma-separated list of fields to exclude from the returned response. Example: `_links,total_items`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        [
          {}
        ]
      ],
      "stores": [
        [
          "string"
        ]
      ],
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links[]` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |
| `links[].targetSchema` | string |  |
| `stores[]` | array<string> |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `GET ecommerce/stores` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-e-commerce-stores.md) for the provider-specific parameters and requirements.

