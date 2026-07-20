# Chatsistant: Delete Multiple Messages

Deletes multiple messages from Chatsistant.

```
DELETE https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/delete-multiple-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatsistant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/delete-multiple-messages?connectionId=$CONNECTION_ID&uuids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/delete-multiple-messages?${params}`, {
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
| `uuids[]` | array<string> | yes | List of message UUIDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Chatsistant API, this operation is `POST /messages/delete` (base URL `https://app.chatsistant.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-multiple-messages.md) for the provider-specific parameters and requirements.

