# xMatters: Modify a form response option

Updates a form response option in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-form-response-option
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-form-response-option" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-form-response-option', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | no |  |
| `allowComments` | boolean | no |  |
| `contribution` | string | no |  |
| `description` | string | no |  |
| `formId` | string | no |  |
| `id` | string | no |  |
| `joinConference` | boolean | no |  |
| `number` | number | no |  |
| `prompt` | string | no |  |
| `text` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "allowComments": true,
      "contribution": "string",
      "description": "string",
      "id": "string",
      "joinConference": true,
      "number": 1,
      "prompt": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `allowComments` | boolean |  |
| `contribution` | string |  |
| `description` | string |  |
| `id` | string |  |
| `joinConference` | boolean |  |
| `number` | number |  |
| `prompt` | string |  |
| `text` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST forms/{formId}/response-options` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-a-form-response-option.md) for the provider-specific parameters and requirements.

