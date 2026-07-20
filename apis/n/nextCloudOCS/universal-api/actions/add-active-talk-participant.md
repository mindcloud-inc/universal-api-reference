# Next Cloud OCS: Add Active Talk Participant

Adds an active talk participant in Next Cloud OCS.

```
POST https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/add-active-talk-participant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/add-active-talk-participant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/add-active-talk-participant', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "ocs": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `ocs` | object |  |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `POST /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/participants/active` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-active-talk-participant.md) for the provider-specific parameters and requirements.

