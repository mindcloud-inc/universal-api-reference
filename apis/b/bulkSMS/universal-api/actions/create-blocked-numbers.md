# BulkSMS: Create Blocked Numbers

Creates blocked phone numbers in BulkSMS.

```
POST https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/create-blocked-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/create-blocked-numbers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blockedNumbers[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/create-blocked-numbers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blockedNumbers[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blockedNumbers[]` | array<object> | yes | Array of blocked-number objects to create. Each item should include phoneNumber and can include description. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BulkSMS API returns.

## Native endpoint

Through the native BulkSMS API, this operation is `POST /blocked-numbers` (base URL `https://api.bulksms.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-blocked-numbers.md) for the provider-specific parameters and requirements.

