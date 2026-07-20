# Myphoner: Mark Lead for Call Back

Marks a lead for call back in Myphoner.

```
PUT https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/mark-lead-for-call-back
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Myphoner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/mark-lead-for-call-back" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/mark-lead-for-call-back', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callBackIn` | number | no | Minutes until the scheduled call back. |
| `category` | string | no | Existing Myphoner category to apply exactly as named. |
| `comment` | string | no | Comment text to attach to the lead event. |
| `leadId` | number | yes | The Myphoner lead ID. |
| `scheduledFor` | date | no | UTC datetime for the scheduled call back. Takes precedence over Call Back In when present. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Myphoner API returns.

## Native endpoint

Through the native Myphoner API, this operation is `POST /leads/:leadId/call_back` (base URL `https://{{credentials.subdomain}}.myphoner.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-lead-for-call-back.md) for the provider-specific parameters and requirements.

