# Saastic: Update Location

Updates an existing location in Saastic.

```
PUT https://connect.mindcloud.co/v1/universal/saastic/latest/actions/update-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Saastic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/saastic/latest/actions/update-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/saastic/latest/actions/update-location', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The location ID. |
| `name` | string | no | The name of the location. |
| `displayName` | string | no | The customer-facing name for the location. Falls back to name. |
| `slug` | string | no | The slug for the location. Generated if left out. |
| `code` | string | no | An optional store code. |
| `address1` | string | no | Address line 1. |
| `address2` | string | no | Address line 2. |
| `city` | string | no | The city or town. |
| `state` | string | no | The state or region. |
| `postalCode` | string | no | The postal code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "address1": "string",
      "address2": "string",
      "city": "string",
      "code": "string",
      "display_name": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "postal_code": "string",
      "project_id": 1,
      "slug": "string",
      "state": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `address1` | string |  |
| `address2` | string |  |
| `city` | string |  |
| `code` | string |  |
| `display_name` | string |  |
| `id` | number |  |
| `name` | string |  |
| `postal_code` | string |  |
| `project_id` | number |  |
| `slug` | string |  |
| `state` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Saastic API, this operation is `PUT /beacon/locations/:id` (base URL `https://api.moregoodreviews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-location.md) for the provider-specific parameters and requirements.

