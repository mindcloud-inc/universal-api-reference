# DitLead: Send Warming Emails



```
PUT https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/send-warming-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/send-warming-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/send-warming-emails', {
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
| `mailboxAddress` | string | no |  |
| `mailboxId` | string | no | Public ID of the mailbox to warm. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native DitLead API, this operation is `POST /v1/mailbox/warming/send` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-warming-emails.md) for the provider-specific parameters and requirements.

