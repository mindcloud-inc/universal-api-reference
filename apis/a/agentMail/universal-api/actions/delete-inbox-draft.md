# Agent Mail: Delete Inbox Draft

Deletes a draft from a specific AgentMail inbox.

```
DELETE https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/delete-inbox-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/delete-inbox-draft?connectionId=$CONNECTION_ID&draftId=string&inboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "draftId": "string",
  "inboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/delete-inbox-draft?${params}`, {
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
| `draftId` | string | yes | The AgentMail draft ID. |
| `inboxId` | string | yes | The AgentMail inbox ID. |

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

Through the native Agent Mail API, this operation is `DELETE /inboxes/{inbox_id}/drafts/{draft_id}` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-inbox-draft.md) for the provider-specific parameters and requirements.

