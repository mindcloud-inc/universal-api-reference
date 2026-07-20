# LEADTEX: Set Contact Variable

Creates or updates a contact variable in LEADTEX.

```
PUT https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/set-contact-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/set-contact-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_id": 1,
  "name": "Ava Chen",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/set-contact-variable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_id": 1,
    "name": "Ava Chen",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact_id` | number | yes | ID of the contact whose variable should be set. |
| `name` | string | yes | Variable name. |
| `value` | string | yes | Variable value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "updated_at": "2026-05-07T12:00:00.000Z",
        "value": "string",
        "variable": {}
      },
      "errors": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.created_at` | date |  |
| `data.id` | number |  |
| `data.updated_at` | date |  |
| `data.value` | string |  |
| `data.variable` | object |  |
| `errors` | object |  |
| `message` | string |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /setContactVariable?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-contact-variable.md) for the provider-specific parameters and requirements.

