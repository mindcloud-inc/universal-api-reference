# DocuPanda - Document Understanding: Update Workspace Member

Updates an existing workspace member in DocuPanda.

```
PUT https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/update-workspace-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/update-workspace-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "memberUserId": "string",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/update-workspace-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "memberUserId": "string",
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Action to perform: 'update_role' or 'remove' |
| `memberUserId` | string | yes | User ID of the member to update |
| `newRole` | string | no | New role for the member (if action is update_role) |
| `workspaceId` | string | yes | ID of the workspace |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string | Response message |
| `name` | string |  |
| `status` | string | Status of the response |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /internal/workspace/member/update` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace-member.md) for the provider-specific parameters and requirements.

