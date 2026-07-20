# Missive: Create Incoming Message

Creates an incoming message in your Missive workspace.

```
POST https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-incoming-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-incoming-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account": "string",
  "body": "string",
  "fromField": {},
  "toFields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/missive/latest/actions/create-incoming-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account": "string",
    "body": "string",
    "fromField": {},
    "toFields": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account` | string | yes | Account ID from the custom channel settings or Missive Resource IDs. |
| `body` | string | yes | Incoming message body as HTML or text. |
| `fromField` | object | yes | Sender object for text or HTML custom channel messages. Include the documented sender fields in the object. |
| `toFields` | list<object> | yes | Recipient array for text or HTML custom channel messages. Include the documented recipient objects in the array. |
| `subject` | string | no | Subject line for email messages only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversation": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversation` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Missive API, this operation is `POST /messages` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-incoming-message.md) for the provider-specific parameters and requirements.

