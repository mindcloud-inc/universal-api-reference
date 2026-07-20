# NeetoCal: Update Duration

Updates an existing meeting duration in NeetoCal.

```
PUT https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/update-meeting-duration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoCal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/update-meeting-duration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "meeting_sid": "string",
  "id": "string",
  "duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/update-meeting-duration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "meeting_sid": "string",
    "id": "string",
    "duration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `meeting_sid` | string | yes | The scheduling link SID. |
| `id` | string | yes | The duration ID. |
| `duration` | number | yes | Updated duration in minutes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NeetoCal API returns.

## Native endpoint

Through the native NeetoCal API, this operation is `PUT /meetings/:meeting_sid/durations/:id` (base URL `https://{{credentials.subdomain}}.neetocal.com/api/external/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-meeting-duration.md) for the provider-specific parameters and requirements.

