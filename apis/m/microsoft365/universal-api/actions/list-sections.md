# Microsoft 365: List Sections

Retrieves OneNote sections from Microsoft 365.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-sections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-sections?${params}`, {
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
| `maxResults` | number | no | Maximum number of sections to return. Default: `10`. |

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

Through the native Microsoft 365 API, this operation is `GET /v1.0/me/onenote/sections` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sections.md) for the provider-specific parameters and requirements.

