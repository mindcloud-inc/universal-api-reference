# Mailtrap: Send Setup Instructions

Sends sending domain setup instructions from Mailtrap.

```
POST https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/send-setup-instructions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailtrap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/send-setup-instructions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/send-setup-instructions', {
  method: 'POST',
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



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mailtrap API returns.

## Native endpoint

Through the native Mailtrap API, this operation is `POST /sending_domains/{sending_domain_id}/send_setup_instructions` (base URL `https://mailtrap.io/api/accounts/:account_id`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-setup-instructions.md) for the provider-specific parameters and requirements.

