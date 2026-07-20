# Digital Samba: Archive recording

Updates a recording to archived in Digital Samba.

```
PUT https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/archive-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/archive-recording" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recording": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/archive-recording', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recording": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recording` | string | yes | Recording path parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digital Samba API returns.

## Native endpoint

Through the native Digital Samba API, this operation is `POST /recordings/:recording/archive` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-recording.md) for the provider-specific parameters and requirements.

