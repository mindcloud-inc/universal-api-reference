# Tellephant: Get message history

Retrieves delivery history for a message in Tellephant.

```
GET https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/get-message-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tellephant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/get-message-history?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/get-message-history?${params}`, {
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
| `messageId` | string | yes | Tellephant message ID to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": {},
      "message": "string",
      "messageId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `error` | object |  |
| `message` | string |  |
| `messageId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tellephant API, this operation is `POST /v1/message-history` (base URL `https://api.tellephant.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-history.md) for the provider-specific parameters and requirements.

