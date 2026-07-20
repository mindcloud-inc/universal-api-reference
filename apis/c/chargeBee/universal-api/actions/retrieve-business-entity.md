# ChargeBee: Retrieve Business Entity

Retrieves a business entity from ChargeBee.

```
GET https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-business-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-business-entity?connectionId=$CONNECTION_ID&business_entity_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "business_entity_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-business-entity?${params}`, {
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
| `business_entity_id` | string | yes | The Chargebee business entity identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "business_entity_id": "string",
      "created_at": 1,
      "deleted": true,
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "status": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `business_entity_id` | string |  |
| `created_at` | number |  |
| `deleted` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `status` | string |  |
| `updated_at` | number |  |

## Native endpoint

Through the native ChargeBee API, this operation is `GET business_entities/:business_entity_id` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-business-entity.md) for the provider-specific parameters and requirements.

