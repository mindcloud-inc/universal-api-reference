# Sendcrux: Add Email List Field

Creates a custom field for an email list in Sendcrux.

```
POST https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/add-email-list-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/add-email-list-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "string",
  "tag": "string",
  "type": "string",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/add-email-list-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "string",
    "tag": "string",
    "type": "string",
    "uid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `default_value` | string | no | The default value for the custom field. |
| `label` | string | yes | The display label for the new custom field. |
| `tag` | string | yes | The unique field tag used by Sendcrux for this custom field. |
| `type` | string | yes | The Sendcrux field type, such as text. |
| `uid` | string | yes | The unique identifier of the list to extend with a custom field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field` | object |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Sendcrux API, this operation is `POST /api/v1/lists/:uid/add-field` (base URL `https://sendcrux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-email-list-field.md) for the provider-specific parameters and requirements.

