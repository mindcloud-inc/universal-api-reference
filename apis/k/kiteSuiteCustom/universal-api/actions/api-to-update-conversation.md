# Kite Suite: Api to update conversation



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/api-to-update-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/api-to-update-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "name": "Ava Chen",
  "memberId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/api-to-update-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "name": "Ava Chen",
    "memberId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `id` | string | no | conversation Id |
| `name` | string | yes |  |
| `memberId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kite Suite API returns.

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/conversation/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/api-to-update-conversation.md) for the provider-specific parameters and requirements.

