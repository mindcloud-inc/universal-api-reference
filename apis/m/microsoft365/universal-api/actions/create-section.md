# Microsoft 365: Create Section

Creates a new section in Microsoft 365.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-section" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "notebookId": "string",
  "displayName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-section', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "notebookId": "string",
    "displayName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notebookId` | string | yes | The target notebook ID. |
| `displayName` | string | yes | The section name to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": {
        "user": {
          "displayName": "Ava Chen"
        }
      },
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "id": "string",
      "isDefault": true,
      "lastModifiedBy": {
        "user": {
          "displayName": "Ava Chen"
        }
      },
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "pagesUrl": "https://example.com",
      "parentNotebook": {
        "displayName": "Ava Chen",
        "id": "string"
      },
      "self": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy.user.displayName` | string | Display name of the section creator. |
| `createdDateTime` | date | When the section was created. |
| `displayName` | string | Section display name. |
| `id` | string | Unique OneNote section ID. |
| `isDefault` | boolean | Whether this is the default section. |
| `lastModifiedBy.user.displayName` | string | Display name of the last user who modified the section. |
| `lastModifiedDateTime` | date | When the section was last modified. |
| `pagesUrl` | string | Graph URL for the section's pages. |
| `parentNotebook.displayName` | string | Name of the parent notebook. |
| `parentNotebook.id` | string | ID of the parent notebook. |
| `self` | string | Microsoft Graph URL for the section. |

## Native endpoint

Through the native Microsoft 365 API, this operation is `POST /v1.0/me/onenote/notebooks/{{notebookId}}/sections` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-section.md) for the provider-specific parameters and requirements.

