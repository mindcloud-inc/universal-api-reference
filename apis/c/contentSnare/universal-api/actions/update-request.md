# Content Snare: Update Request

Updates a request in Content Snare.

```
PUT https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/update-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/update-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/update-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Request ID. |
| `clientAssignmentsIds[]` | array<object> | no | Client Assignments Ids. |
| `clientAssignmentsIds[].accountId` | string | no | Client id |
| `clientAssignmentsIds[].clientCompanyId` | string | no | Client company id |
| `clientAssignmentsIds[].primary` | boolean | no | Set true to mark client as primary. Only one client in request can be primary. |
| `commentsEnabled` | boolean | no | Enable client comments. This allows your client to ask questions about each field. |
| `communicationTemplateId` | string | no | Id of communications schedule. Set this parameter as null to remove existing communications schedule from request. |
| `communicationTemplateName` | string | no | Name of communications schedule. Set this parameter as null or "None" to remove existing communications schedule from request. |
| `due` | date | no | Due date for the request. <br><b>Format:</b> yyyy-mm-dd |
| `folderId` | string | no | Folder id. Requests may be grouped in to folders on the requests page. Don't send it if you do not wish to group your Requests. |
| `folderName` | string | no | Folder name. Requests may be grouped in to folders on the requests page. Don't send it if you do not wish to group your Requests. |
| `instructionText` | string | no | Request instructions are the first thing your client will see when they open the request. Use this area to let them know who you are, what the request is for, and provide some simple instructions on how to use Content Snare. |
| `name` | string | no | Request name |
| `ownerId` | string | no | Request owner (team member) id |
| `ownerEmail` | string | no | Request owner (team member) email |
| `passcodeEnabled` | boolean | no | Protect share with a pin code. Your client will be asked to set their own pincode when they first access the request. |
| `shareViaLinkEnabled` | boolean | no | Allow share via link without requiring login |
| `showInstruction` | boolean | no | Enable request instructions |
| `status` | string | no | Request status |
| `updatedAt` | date | no | Updated At. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author_name": "Ava Chen",
      "client_status": "string",
      "client": {
        "avatar": "string",
        "company_name": "Ava Chen",
        "email": "ava@example.com",
        "full_name": "Ava Chen",
        "id": "string",
        "phone": "string",
        "url": "https://example.com"
      },
      "clients": [
        {
          "avatar": "string",
          "company_name": "Ava Chen",
          "email": "ava@example.com",
          "full_name": "Ava Chen",
          "id": "string",
          "phone": "string",
          "url": "https://example.com"
        }
      ],
      "comments_enabled": true,
      "communications_template_name": "Ava Chen",
      "completion_percentage": 1,
      "due": "2026-05-07T12:00:00.000Z",
      "folder_name": "Ava Chen",
      "id": "string",
      "instruction_text": "string",
      "name": "Ava Chen",
      "owner_name": "Ava Chen",
      "passcode_enabled": true,
      "request_template_name": "Ava Chen",
      "share_link": "https://example.com",
      "share_via_link_enabled": true,
      "show_instruction": true,
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author_name` | string |  |
| `client_status` | string |  |
| `client.avatar` | string |  |
| `client.company_name` | string |  |
| `client.email` | string |  |
| `client.full_name` | string |  |
| `client.id` | string |  |
| `client.phone` | string |  |
| `client.url` | string |  |
| `clients[].avatar` | string |  |
| `clients[].company_name` | string |  |
| `clients[].email` | string |  |
| `clients[].full_name` | string |  |
| `clients[].id` | string |  |
| `clients[].phone` | string |  |
| `clients[].url` | string |  |
| `comments_enabled` | boolean |  |
| `communications_template_name` | string |  |
| `completion_percentage` | number |  |
| `due` | date |  |
| `folder_name` | string |  |
| `id` | string |  |
| `instruction_text` | string |  |
| `name` | string |  |
| `owner_name` | string |  |
| `passcode_enabled` | boolean |  |
| `request_template_name` | string |  |
| `share_link` | string |  |
| `share_via_link_enabled` | boolean |  |
| `show_instruction` | boolean |  |
| `status` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Content Snare API, this operation is `PUT /partner_api/v1/requests/{id}` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-request.md) for the provider-specific parameters and requirements.

