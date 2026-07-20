# MS SharePoint: Get Drive

Retrieves a SharePoint drive.

```
GET https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-drive
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MS SharePoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-drive?connectionId=$CONNECTION_ID&driveId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driveId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-drive?${params}`, {
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
| `driveId` | string | yes | Microsoft Graph drive ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": {},
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "driveType": "string",
      "id": "string",
      "lastModifiedBy": {},
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "owner": {},
      "quota": {},
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | object |  |
| `createdDateTime` | date |  |
| `driveType` | string |  |
| `id` | string |  |
| `lastModifiedBy` | object |  |
| `lastModifiedDateTime` | date |  |
| `name` | string |  |
| `owner` | object |  |
| `quota` | object |  |
| `webUrl` | string |  |

## Native endpoint

Through the native MS SharePoint API, this operation is `GET /v1.0/drives/{{driveId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-drive.md) for the provider-specific parameters and requirements.

