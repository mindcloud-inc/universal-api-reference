# Vybit: Invite User to Vybit



```
POST https://connect.mindcloud.co/v1/universal/vybit/latest/actions/invite-user-to-vybit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/invite-user-to-vybit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vybit/latest/actions/invite-user-to-vybit', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address of the user to invite to the vybit. |
| `key` | string | yes | The unique key of the vybit to invite a user to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "logKey": "string",
      "message": "string",
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string | Key of the created peep. |
| `logKey` | string | Key of the log entry created for the invitation. |
| `message` | string | Outcome message from Vybit. |
| `result` | number | Result code for the invitation request. |

## Native endpoint

Through the native Vybit API, this operation is `POST /peep/{{key}}` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-user-to-vybit.md) for the provider-specific parameters and requirements.

