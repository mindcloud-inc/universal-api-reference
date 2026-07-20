# Microsoft SharePoint Online: Search Sites

Finds sites in Microsoft SharePoint Online by keyword.

```
GET https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/search-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft SharePoint Online `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/search-sites?connectionId=$CONNECTION_ID&limit=25&offset=0&search=marketing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "search": "marketing"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/search-sites?${params}`, {
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
| `search` | string | yes | Search text used by Microsoft Graph to find SharePoint sites. Example: `marketing`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "root": {},
      "siteCollection": {},
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDateTime` | date |  |
| `description` | string |  |
| `displayName` | string |  |
| `id` | string |  |
| `lastModifiedDateTime` | date |  |
| `name` | string |  |
| `root` | object |  |
| `siteCollection` | object |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Microsoft SharePoint Online API, this operation is `GET /v1.0/sites` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-sites.md) for the provider-specific parameters and requirements.

