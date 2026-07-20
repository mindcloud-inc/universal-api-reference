# Maildrip: Import contact groups to an instant email



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/import-contact-groups-to-an-instant-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/import-contact-groups-to-an-instant-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailId": "ava@example.com",
  "groups[]": [
    "string"
  ],
  "recipients[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/import-contact-groups-to-an-instant-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailId": "ava@example.com",
    "groups[]": ["string"],
    "recipients[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailId` | string | yes | ID of the instant email to import groups into |
| `groups[]` | array<string> | yes | List of group IDs to import Accepts multiple values as an array. |
| `recipients[]` | array<string> | yes | List of recipient email addresses Accepts multiple values as an array. |

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
| `data` | object | Data returned from the processor server |
| `message` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/instant-emails/save-groups/{emailId}` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-contact-groups-to-an-instant-email.md) for the provider-specific parameters and requirements.

