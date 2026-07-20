# SimpleCert: Create Recipient



```
POST https://connect.mindcloud.co/v1/universal/simpleCert/latest/actions/create-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleCert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleCert/latest/actions/create-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "firstName": "Ava",
  "lastName": "Chen",
  "emailAddress": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleCert/latest/actions/create-recipient', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "firstName": "Ava",
    "lastName": "Chen",
    "emailAddress": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | Project identifier. |
| `firstName` | string | yes | Recipient first name. |
| `lastName` | string | yes | Recipient last name. |
| `emailAddress` | string | yes | Recipient email address. |
| `dontSendEmail` | string | no | Set to true to suppress the outbound recipient email. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SimpleCert API returns.

## Native endpoint

Through the native SimpleCert API, this operation is `POST /projects/:project_id/recipient/add` (base URL `https://app.simplecert.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recipient.md) for the provider-specific parameters and requirements.

