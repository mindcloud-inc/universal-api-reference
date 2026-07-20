# Microsoft 365: List Notebooks

Retrieves notebooks from Microsoft 365.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-notebooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-notebooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-notebooks?${params}`, {
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
| `maxResults` | number | no | Maximum number of notebooks to return. Default: `10`. |

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
      "isShared": true,
      "lastModifiedBy": {
        "user": {
          "displayName": "Ava Chen"
        }
      },
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "links": {
        "oneNoteWebUrl": {
          "href": "https://example.com"
        }
      },
      "sectionGroupsUrl": "https://example.com",
      "sectionsUrl": "https://example.com",
      "self": "string",
      "userRole": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy.user.displayName` | string | Display name of the notebook creator. |
| `createdDateTime` | date | When the notebook was created. |
| `displayName` | string | Notebook display name. |
| `id` | string | Unique OneNote notebook ID. |
| `isDefault` | boolean | Whether this is the default notebook. |
| `isShared` | boolean | Whether the notebook is shared. |
| `lastModifiedBy.user.displayName` | string | Display name of the last user who modified the notebook. |
| `lastModifiedDateTime` | date | When the notebook was last modified. |
| `links.oneNoteWebUrl.href` | string | Web URL for opening the notebook in OneNote. |
| `sectionGroupsUrl` | string | Graph URL for the notebook's section groups. |
| `sectionsUrl` | string | Graph URL for the notebook's sections. |
| `self` | string | Microsoft Graph URL for the notebook. |
| `userRole` | string | The signed-in user's role for the notebook. |

## Native endpoint

Through the native Microsoft 365 API, this operation is `GET /v1.0/me/onenote/notebooks` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notebooks.md) for the provider-specific parameters and requirements.

