# Innform: Update Property

Updates an existing property in Innform.

```
PUT https://connect.mindcloud.co/v1/universal/innform/latest/actions/update-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Innform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/innform/latest/actions/update-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/innform/latest/actions/update-property', {
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
| `address` | string | no | Updated property address. |
| `city` | string | no | Updated property city. |
| `country` | string | no | Updated property country. |
| `id` | string | yes | Property UUID. |
| `name` | string | no | Updated property name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "country": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Property address. |
| `city` | string | Property city. |
| `country` | string | Property country. |
| `id` | string | Property ID. |
| `name` | string | Property name. |

## Native endpoint

Through the native Innform API, this operation is `PUT /properties/{id}` (base URL `https://api.innform.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-property.md) for the provider-specific parameters and requirements.

