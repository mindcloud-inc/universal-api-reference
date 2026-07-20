# Aloware: Establish Two-Legged Call

Establishes a two-legged call in Aloware.

```
POST https://connect.mindcloud.co/v1/universal/aloware/latest/actions/establish-two-legged-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aloware `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/establish-two-legged-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aloware/latest/actions/establish-two-legged-call', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | no | User ID for the agent leg. Provide this or Ring Group ID. |
| `ringGroupId` | string | no | Ring group ID for the agent leg. Provide this or User ID. |
| `contactPhoneNumber` | string | no | Contact phone number. Provide this or Contact ID. |
| `contactId` | string | no | Contact ID. Provide this or Contact Phone Number. |
| `linePhoneNumber` | string | no | Aloware line phone number. Provide this or Line ID. |
| `lineId` | string | no | Aloware line ID. Provide this or Line Phone Number. |
| `userPhoneNumber` | string | no | Optional user phone number when starting a call with User ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aloware API returns.

## Native endpoint

Through the native Aloware API, this operation is `POST /api/v1/webhook/two-legged-call` (base URL `https://app.aloware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/establish-two-legged-call.md) for the provider-specific parameters and requirements.

