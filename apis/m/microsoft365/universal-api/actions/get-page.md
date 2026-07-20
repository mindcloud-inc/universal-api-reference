# Microsoft 365: Get Page

Retrieves a OneNote page from Microsoft 365.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-page?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-page?${params}`, {
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
| `pageId` | string | yes | The OneNote page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentUrl": "https://example.com",
      "createdByAppId": "string",
      "id": "string",
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "links": {
        "oneNoteClientUrl": {
          "href": "https://example.com"
        },
        "oneNoteWebUrl": {
          "href": "https://example.com"
        }
      },
      "parentNotebook": {
        "displayName": "Ava Chen",
        "id": "string"
      },
      "parentSection": {
        "displayName": "Ava Chen",
        "id": "string",
        "self": "string"
      },
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentUrl` | string | URL for the page content. |
| `createdByAppId` | string | App ID that created the page, when available. |
| `id` | string | Unique OneNote page ID. |
| `lastModifiedDateTime` | date | When the page was last modified. |
| `links.oneNoteClientUrl.href` | string | OneNote client URL for the page. |
| `links.oneNoteWebUrl.href` | string | OneNote web URL for the page. |
| `parentNotebook.displayName` | string | Name of the parent notebook. |
| `parentNotebook.id` | string | ID of the parent notebook. |
| `parentSection.displayName` | string | Name of the parent section. |
| `parentSection.id` | string | ID of the parent section. |
| `parentSection.self` | string | Graph URL for the parent section. |
| `title` | string | Page title. |

## Native endpoint

Through the native Microsoft 365 API, this operation is `GET /v1.0/me/onenote/pages/{{pageId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

