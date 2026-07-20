# Callingly: Create Call

Creates a call in Callingly.

```
POST https://connect.mindcloud.co/v1/universal/callingly/latest/actions/create-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/create-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "19230",
  "firstName": "John",
  "lastName": "Doe",
  "phoneNumber": "+15555550100"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callingly/latest/actions/create-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "19230",
    "firstName": "John",
    "lastName": "Doe",
    "phoneNumber": "+15555550100"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | number | yes | Team that should receive the created call. Example: `19230`. |
| `firstName` | string | yes | Example: `John`. |
| `lastName` | string | yes | Example: `Doe`. |
| `phoneNumber` | string | yes | Example: `+15555550100`. |
| `email` | string | no | Example: `john@example.com`. |
| `company` | string | no | Example: `Example Company`. |
| `category` | string | no | Example: `Website`. |
| `source` | string | no | Example: `MindCloud Test`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | no | Agency partner account ID for requests on behalf of a client account. Example: `12345`. |
| `crmId` | number | no | Example: `123`. |
| `scheduledAt` | string | no | Optional schedule timestamp for the call. Example: `2026-03-20 15:30:00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "call_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `call_id` | number | ID of the created call. |

## Native endpoint

Through the native Callingly API, this operation is `POST /v1/calls` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-call.md) for the provider-specific parameters and requirements.

