# Superglue: Send Portal Invitation Email



```
POST https://connect.mindcloud.co/v1/universal/superglue/latest/actions/send-portal-invitation-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superglue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/send-portal-invitation-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endUserId": "550e8400-e29b-41d4-a716-446655440000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superglue/latest/actions/send-portal-invitation-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endUserId": "550e8400-e29b-41d4-a716-446655440000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endUserId` | string | yes | Internal Superglue end-user ID. Example: `550e8400-e29b-41d4-a716-446655440000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "recipient": "ava@example.com",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message for the invitation request. |
| `recipient` | string | Email recipient of the portal invitation. |
| `success` | boolean | Whether the invitation email was sent. |

## Native endpoint

Through the native Superglue API, this operation is `POST /end-users/:endUserId/invite` (base URL `https://api.superglue.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-portal-invitation-email.md) for the provider-specific parameters and requirements.

