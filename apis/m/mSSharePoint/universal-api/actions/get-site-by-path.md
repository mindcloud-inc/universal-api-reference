# MS SharePoint: Get Site By Path

Retrieves a SharePoint site by path.

```
GET https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-site-by-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MS SharePoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-site-by-path?connectionId=$CONNECTION_ID&hostname=Ava%20Chen&relativePath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hostname": "Ava Chen",
  "relativePath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-site-by-path?${params}`, {
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
| `hostname` | string | yes | SharePoint hostname, for example contoso.sharepoint.com. |
| `relativePath` | string | yes | Site path relative to the hostname, for example sites/project-x. |

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
      "sharepointIds": {},
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
| `sharepointIds` | object |  |
| `siteCollection` | object |  |
| `webUrl` | string |  |

## Native endpoint

Through the native MS SharePoint API, this operation is `GET /v1.0/sites/{{hostname}}:/{{relativePath}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-by-path.md) for the provider-specific parameters and requirements.

