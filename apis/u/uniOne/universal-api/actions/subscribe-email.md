# UniOne: Subscribe Email

Subscribes an email address through UniOne.

```
POST https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/subscribe-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/subscribe-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromEmail": "no-reply@mindcloud.co",
  "fromName": "MindCloud",
  "toEmail": "apps@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/subscribe-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromEmail": "no-reply@mindcloud.co",
    "fromName": "MindCloud",
    "toEmail": "apps@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromEmail` | string | yes | Sender email address. Example: `no-reply@mindcloud.co`. |
| `fromName` | string | yes | Sender name. Example: `MindCloud`. |
| `toEmail` | string | yes | Recipient email address. Example: `apps@mindcloud.co`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UniOne API returns.

## Native endpoint

Through the native UniOne API, this operation is `POST email/subscribe.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-email.md) for the provider-specific parameters and requirements.

