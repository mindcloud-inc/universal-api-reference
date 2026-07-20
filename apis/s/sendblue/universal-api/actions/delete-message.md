# Sendblue: Delete Message

Soft deletes a message from Sendblue.

```
DELETE https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/delete-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/delete-message?connectionId=$CONNECTION_ID&messageHandle=13bb119a-d6c4-45b9-b8cd-54a6b8be0965" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageHandle": "13bb119a-d6c4-45b9-b8cd-54a6b8be0965"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/delete-message?${params}`, {
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
| `messageHandle` | string | yes | Message handle to delete. Example: `13bb119a-d6c4-45b9-b8cd-54a6b8be0965`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `DELETE /api/message/:message_handle` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message.md) for the provider-specific parameters and requirements.

