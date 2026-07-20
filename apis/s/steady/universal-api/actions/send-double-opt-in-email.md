# Steady: Send Double Opt-In Email

Sends a double opt-in email from Steady.

```
POST https://connect.mindcloud.co/v1/universal/steady/latest/actions/send-double-opt-in-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Steady `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/steady/latest/actions/send-double-opt-in-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/steady/latest/actions/send-double-opt-in-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The email address of the prospective newsletter subscriber. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "email": "ava@example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.email` | string |  |

## Native endpoint

Through the native Steady API, this operation is `POST /newsletter_subscribers/send_double_opt_in_email` (base URL `https://steadyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-double-opt-in-email.md) for the provider-specific parameters and requirements.

