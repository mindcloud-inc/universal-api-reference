# Statsig: Update change validation message

Updates a change validation message in Statsig.

```
PUT https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-change-validation-message-patch-console-v1-change-validation-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-change-validation-message-patch-console-v1-change-validation-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reviewID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-change-validation-message-patch-console-v1-change-validation-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reviewID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reviewID` | string | yes | Request body field. |
| `message` | string | no | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `PATCH /console/v1/change_validation/message` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-change-validation-message-patch-console-v1-change-validation-message.md) for the provider-specific parameters and requirements.

