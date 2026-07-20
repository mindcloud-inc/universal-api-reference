# Lemcal: Create Hook

Creates a new hook in Lemcal.

```
POST https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/create-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lemcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/create-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/create-hook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetUrl` | string | yes | The callback URL for the hook. |
| `meetingTypeId` | string | no | A specific meeting type to associate with the hook. |
| `anyMeetingType` | boolean | no | Apply the hook to any meeting type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "anyMeetingType": true,
      "createdAt": "string",
      "meetingTypeId": "string",
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `anyMeetingType` | boolean |  |
| `createdAt` | string |  |
| `meetingTypeId` | string |  |
| `targetUrl` | string |  |

## Native endpoint

Through the native Lemcal API, this operation is `POST /hooks` (base URL `https://api.lemcal.com/api/lemcal`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-hook.md) for the provider-specific parameters and requirements.

