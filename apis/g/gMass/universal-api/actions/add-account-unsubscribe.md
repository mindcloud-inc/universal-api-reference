# GMass: Add Account Unsubscribe

Adds an address to your GMass unsubscribe list.

```
POST https://connect.mindcloud.co/v1/universal/gMass/latest/actions/add-account-unsubscribe
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/add-account-unsubscribe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailAddress": "gmass-stage3@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gMass/latest/actions/add-account-unsubscribe', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailAddress": "gmass-stage3@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailAddress` | string | yes | Email address to add to the account-wide unsubscribe list. Example: `gmass-stage3@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailAddress": "ava@example.com",
      "sender": "string",
      "unsubscribeTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddress` | string | Email address on the account unsubscribe list. |
| `sender` | string | Sender associated with the unsubscribe record when available. |
| `unsubscribeTime` | date | Time the unsubscribe record was created. |

## Native endpoint

Through the native GMass API, this operation is `POST /unsubscribes` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-account-unsubscribe.md) for the provider-specific parameters and requirements.

