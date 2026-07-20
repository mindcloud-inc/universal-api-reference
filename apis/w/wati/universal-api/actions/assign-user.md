# Wati: Assign User

Updates a conversation assignment in Wati.

```
PUT https://connect.mindcloud.co/v1/universal/wati/latest/actions/assign-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wati/latest/actions/assign-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "whatsappNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wati/latest/actions/assign-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "whatsappNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address of the operator to assign. |
| `whatsappNumber` | string | yes | Target WhatsApp phone number for the assignment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `info` | string | Provider message for the assignment attempt. |
| `result` | boolean | Whether Wati accepted the assignment request. |

## Native endpoint

Through the native Wati API, this operation is `POST /api/v1/assignOperator` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-user.md) for the provider-specific parameters and requirements.

