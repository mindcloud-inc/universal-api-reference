# ThriveDesk: Delete Assistant



```
DELETE https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/delete-assistant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/delete-assistant?connectionId=$CONNECTION_ID&assistantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assistantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/delete-assistant?${params}`, {
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
| `assistantId` | string | yes | The assistant ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Response payload. |
| `id` | string | Resource identifier when returned. |
| `message` | string | Response message. |
| `success` | boolean | Whether the operation succeeded. |

## Native endpoint

Through the native ThriveDesk API, this operation is `DELETE /v1/assistants/{{assistantId}}` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-assistant.md) for the provider-specific parameters and requirements.

