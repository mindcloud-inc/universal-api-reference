# Callbell: Get Message Status

Retrieves message status details from Callbell.

```
GET https://connect.mindcloud.co/v1/universal/callbell/latest/actions/get-message-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callbell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callbell/latest/actions/get-message-status?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callbell/latest/actions/get-message-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | Identifier of the message sent through the API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {},
      "conversation": {},
      "messageStatusPayload": {},
      "status": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object |  |
| `conversation` | object |  |
| `messageStatusPayload` | object |  |
| `status` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Callbell API, this operation is `GET /messages/status/:uuid` (base URL `https://api.callbell.eu/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-status.md) for the provider-specific parameters and requirements.

