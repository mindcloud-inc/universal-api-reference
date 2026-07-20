# KEYZY: Update License Time

Updates start and end times for a KEYZY license.

```
PUT https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/update-license-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KEYZY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/update-license-time" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endAt": 1,
  "serial": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/update-license-time', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endAt": 1,
    "serial": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endAt` | number | yes | License end time as a Unix timestamp. |
| `serial` | string | yes | License serial number. |
| `startAt` | number | no | License start time as a Unix timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | License time update confirmation message. |

## Native endpoint

Through the native KEYZY API, this operation is `POST /licenses/update-time` (base URL `https://api.keyzy.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-license-time.md) for the provider-specific parameters and requirements.

