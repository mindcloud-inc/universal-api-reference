# Sendblue: Get Message Status

Retrieves the status of a message from Sendblue.

```
GET https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/get-message-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/get-message-status?connectionId=$CONNECTION_ID&handle=13bb119a-d6c4-45b9-b8cd-54a6b8be0965" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "13bb119a-d6c4-45b9-b8cd-54a6b8be0965"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/get-message-status?${params}`, {
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
| `handle` | string | yes | Message handle returned by Sendblue when the message was created. Example: `13bb119a-d6c4-45b9-b8cd-54a6b8be0965`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageHandle": "string",
      "status": {
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageHandle` | string |  |
| `status.status` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `GET /api/status` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-status.md) for the provider-specific parameters and requirements.

