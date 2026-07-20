# MS SharePoint: List Site Lists

Retrieves lists for a SharePoint site.

```
GET https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-site-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MS SharePoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-site-lists?connectionId=$CONNECTION_ID&limit=25&offset=0&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-site-lists?${params}`, {
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
| `siteId` | string | yes | Microsoft Graph SharePoint site ID. |

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
      "list": {},
      "name": "Ava Chen",
      "sharepointIds": {},
      "system": {},
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
| `list` | object |  |
| `name` | string |  |
| `sharepointIds` | object |  |
| `system` | object |  |
| `webUrl` | string |  |

## Native endpoint

Through the native MS SharePoint API, this operation is `GET /v1.0/sites/{{siteId}}/lists` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-site-lists.md) for the provider-specific parameters and requirements.

