# BoardCRM: Update Deal Field

Updates an existing deal field in BoardCRM.

```
PUT https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/update-deal-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoardCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/update-deal-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/update-deal-field', {
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
| `id` | number | yes | Field ID. |
| `title` | string | no | Updated field title. |
| `sorting` | number | no | Updated field sort order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "entity": "string",
      "from_api": true,
      "id": 1,
      "is_hidden": true,
      "max_length": 1,
      "options": [
        {}
      ],
      "protected": true,
      "required": true,
      "sorting": 1,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `entity` | string |  |
| `from_api` | boolean |  |
| `id` | number |  |
| `is_hidden` | boolean |  |
| `max_length` | number |  |
| `options` | array<object> |  |
| `protected` | boolean |  |
| `required` | boolean |  |
| `sorting` | number |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native BoardCRM API, this operation is `POST /field/update` (base URL `https://api.boardcrm.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal-field.md) for the provider-specific parameters and requirements.

