# Klenty: Stop Cadence For Prospect

Stops cadence for a prospect in Klenty.

```
PUT https://connect.mindcloud.co/v1/universal/klenty/latest/actions/stop-cadence-for-prospect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/stop-cadence-for-prospect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/klenty/latest/actions/stop-cadence-for-prospect', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cadenceName` | string | no | Cadence name to stop for the prospect. Leave empty to remove from all cadences. |
| `email` | string | yes | Prospect email to remove from a cadence. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {
          "errorCode": "string",
          "errorMessage": "string",
          "type": "string"
        }
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors[].errorCode` | string |  |
| `errors[].errorMessage` | string |  |
| `errors[].type` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Klenty API, this operation is `POST /stopcadence` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-cadence-for-prospect.md) for the provider-specific parameters and requirements.

