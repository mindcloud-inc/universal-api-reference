# NetHunt CRM: Add Gmail Thread to Record

Adds a Gmail thread to a NetHunt CRM record.

```
PUT https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/add-gmail-thread-to-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetHunt CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/add-gmail-thread-to-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "gmailThreadId": "string",
  "recordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/add-gmail-thread-to-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "gmailThreadId": "string",
    "recordId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `gmailThreadId` | string | yes | Gmail conversation ID to link with the record. |
| `recordId` | string | yes | Record ID to link with a Gmail thread. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetHunt CRM API returns.

## Native endpoint

Through the native NetHunt CRM API, this operation is `POST /actions/link-gmail-thread/:recordId` (base URL `https://nethunt.com/api/v1/zapier`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-gmail-thread-to-record.md) for the provider-specific parameters and requirements.

