# Dialpad: Initiate Call

Initiates an outbound call from a Dialpad user.

```
POST https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/initiate-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/initiate-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/initiate-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The user's id. 'me' can be used if you are using a user level API key. |
| `group_id` | number | no | The ID of a group that will be used to initiate the call. |
| `group_type` | string | no | The type of a group that will be used to initiate the call. |
| `phone_number` | string | no | The E164-formatted number to call. |
| `outbound_caller_id` | string | no | The E164-formatted number shown to the call recipient, or 'blocked'. |
| `custom_data` | string | no | Extra data to associate with the call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "device": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `device` | object | The device used to initiate the call. |

## Native endpoint

Through the native Dialpad API, this operation is `POST /users/:id/initiate_call` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initiate-call.md) for the provider-specific parameters and requirements.

