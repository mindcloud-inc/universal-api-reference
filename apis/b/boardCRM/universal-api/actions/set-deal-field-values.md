# BoardCRM: Set Deal Field Values

Updates field values for a deal in BoardCRM.

```
PUT https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/set-deal-field-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoardCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/set-deal-field-values" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/set-deal-field-values', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Deal ID. |
| `fields.title` | string | no | Deal title field value. |
| `fields.description` | string | no | Deal description field value. Pass null to clear it. |
| `fields.price` | number | no | Deal price field value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "price": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `price` | number |  |
| `title` | string |  |

## Native endpoint

Through the native BoardCRM API, this operation is `POST /offer/set-values` (base URL `https://api.boardcrm.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-deal-field-values.md) for the provider-specific parameters and requirements.

