# Microsoft Teams: Get Channel Files Folder

Retrieves a channel's files folder from Microsoft Teams.

```
GET https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/get-channel-files-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/get-channel-files-folder?connectionId=$CONNECTION_ID&teamId=string&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/get-channel-files-folder?${params}`, {
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
| `teamId` | string | yes | Microsoft Graph team ID. |
| `channelId` | string | yes | Microsoft Graph channel ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": {},
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "eTag": "string",
      "folder": {},
      "id": "string",
      "lastModifiedBy": {},
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "parentReference": {},
      "size": 1,
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | object | Identity set for the creator. |
| `createdDateTime` | date | Timestamp at which the item was created. |
| `eTag` | string | ETag for the item metadata and content. |
| `folder` | object | Folder facet when the item is a folder. |
| `id` | string | Unique identifier of the drive item. |
| `lastModifiedBy` | object | Identity set for the last modifier. |
| `lastModifiedDateTime` | date | Timestamp at which the item was last modified. |
| `name` | string | Name of the folder or item. |
| `parentReference` | object | Reference to the parent item. |
| `size` | number | Size of the item in bytes. |
| `webUrl` | string | Browser URL for the drive item. |

## Native endpoint

Through the native Microsoft Teams API, this operation is `GET /v1.0/teams/:teamId/channels/:channelId/filesFolder` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel-files-folder.md) for the provider-specific parameters and requirements.

