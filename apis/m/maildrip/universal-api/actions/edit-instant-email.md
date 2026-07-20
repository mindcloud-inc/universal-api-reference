# Maildrip: Edit instant email



```
PUT https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/edit-instant-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/edit-instant-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailId": "ava@example.com",
  "from": "string",
  "to": "string",
  "subject": "string",
  "typeOfMail": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/edit-instant-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailId": "ava@example.com",
    "from": "string",
    "to": "string",
    "subject": "string",
    "typeOfMail": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailId` | string | yes | ID of the instant email to edit |
| `from` | string | yes |  |
| `to` | string | yes |  |
| `subject` | string | yes |  |
| `body` | string | no |  |
| `status` | string | no |  |
| `typeOfMail` | string | yes |  |
| `selectTemplate` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
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
| `message` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `PATCH /api/v1/instant-emails/{emailId}` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-instant-email.md) for the provider-specific parameters and requirements.

