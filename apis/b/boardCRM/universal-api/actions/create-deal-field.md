# BoardCRM: Create Deal Field

Creates a new deal field in BoardCRM.

```
POST https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/create-deal-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoardCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/create-deal-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/create-deal-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Field title. |

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

Through the native BoardCRM API, this operation is `POST /field/create` (base URL `https://api.boardcrm.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal-field.md) for the provider-specific parameters and requirements.

