# DocuPanda - Document Understanding: Add Workspace Member

Creates a workspace member in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/add-workspace-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/add-workspace-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "memberEmail": "ava@example.com",
  "memberUserId": "string",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/add-workspace-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "memberEmail": "ava@example.com",
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
| `invitedByEmail` | string | no | Email of the inviter |
| `memberEmail` | string | yes | Email of the member to add |
| `memberName` | string | no | Name of the member |
| `memberUserId` | string | yes | User ID of the member |
| `role` | string | no | Role to assign to the member |
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

Through the native DocuPanda - Document Understanding API, this operation is `POST /internal/workspace/member/add` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-workspace-member.md) for the provider-specific parameters and requirements.

