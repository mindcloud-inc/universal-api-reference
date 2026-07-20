# Reloadify: List Custom Attributes

Retrieves custom attributes from Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-custom-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-custom-attributes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-custom-attributes?${params}`, {
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
      "datatype": "string",
      "description": "string",
      "handle": "string",
      "name": "Ava Chen",
      "resource": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datatype` | string |  |
| `description` | string |  |
| `handle` | string |  |
| `name` | string |  |
| `resource` | string |  |

## Native endpoint

Through the native Reloadify API, this operation is `GET /v2/custom_attributes` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-custom-attributes.md) for the provider-specific parameters and requirements.

