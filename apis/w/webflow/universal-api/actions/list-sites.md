# Webflow: List Sites

Retrieves a list of sites from Webflow.

```
GET https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-sites?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "customDomains": [
        {}
      ],
      "dataCollectionEnabled": true,
      "dataCollectionType": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "lastPublished": "2026-05-07T12:00:00.000Z",
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "locales": {},
      "parentFolderId": "string",
      "previewUrl": "https://example.com",
      "shortName": "Ava Chen",
      "timeZone": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date | Creation timestamp. |
| `customDomains` | array<object> | Custom domain entries. |
| `dataCollectionEnabled` | boolean | Whether data collection is enabled. |
| `dataCollectionType` | string | Data collection mode. |
| `displayName` | string | Site display name. |
| `id` | string | Site ID. |
| `lastPublished` | date | Last publish timestamp, if published. |
| `lastUpdated` | date | Last update timestamp. |
| `locales` | object | Locale configuration object. |
| `parentFolderId` | string | Parent folder identifier. |
| `previewUrl` | string | Preview image URL. |
| `shortName` | string | Short slug-like name. |
| `timeZone` | string | Site timezone. |
| `workspaceId` | string | Workspace ID. |

## Native endpoint

Through the native Webflow API, this operation is `GET /sites` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

