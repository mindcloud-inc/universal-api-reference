# ThriveDesk: Delete Inbox Settings



```
DELETE https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/delete-inbox-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/delete-inbox-settings?connectionId=$CONNECTION_ID&inboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/delete-inbox-settings?${params}`, {
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
| `inboxId` | string | yes | The inbox ID. |

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
| `data` | object | Raw response payload when returned. |
| `id` | string | Affected record identifier when returned. |
| `message` | string | Provider response message when returned. |
| `success` | boolean | Whether the request completed successfully. |

## Native endpoint

Through the native ThriveDesk API, this operation is `DELETE /v1/settings/inbox/{{inboxId}}` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-inbox-settings.md) for the provider-specific parameters and requirements.

