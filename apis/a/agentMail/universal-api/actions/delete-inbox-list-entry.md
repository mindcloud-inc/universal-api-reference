# Agent Mail: Delete Inbox List Entry

Deletes an inbox list entry from a specific AgentMail inbox.

```
DELETE https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/delete-inbox-list-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/delete-inbox-list-entry?connectionId=$CONNECTION_ID&direction=string&entry=string&inboxId=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "direction": "string",
  "entry": "string",
  "inboxId": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/delete-inbox-list-entry?${params}`, {
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
| `direction` | string | yes | List direction: send, receive, or reply. |
| `entry` | string | yes | Email address or domain entry. |
| `inboxId` | string | yes | The AgentMail inbox ID. |
| `type` | string | yes | List type: allow or block. |

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
| `success` | boolean | Successful no-body response acknowledged by the wrapper. |

## Native endpoint

Through the native Agent Mail API, this operation is `DELETE /inboxes/{inbox_id}/lists/{direction}/{type}/{entry}` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-inbox-list-entry.md) for the provider-specific parameters and requirements.

