# Productboard: List Custom Fields by Type

Retrieves custom fields for a Productboard hierarchy type.

```
GET https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-custom-fields-by-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-custom-fields-by-type?connectionId=$CONNECTION_ID&type=text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "text"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-custom-fields-by-type?${params}`, {
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
| `type` | string | yes | Field type filter for Productboard custom fields. Allowed values: text, custom-description, number, dropdown, multi-dropdown, member. Default: `text`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "links": {},
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Custom field description. |
| `id` | string | Productboard custom field identifier. |
| `links` | object | Link object for the custom field resource. |
| `name` | string | Custom field name. |
| `type` | string | Productboard custom field type. |

## Native endpoint

Through the native Productboard API, this operation is `GET /hierarchy-entities/custom-fields` (base URL `https://api.productboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-fields-by-type.md) for the provider-specific parameters and requirements.

