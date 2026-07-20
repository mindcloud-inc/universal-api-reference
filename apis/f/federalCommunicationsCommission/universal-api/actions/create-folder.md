# Federal Communications Commission: Create Folder

Creates a new FCC OPIF folder.

```
POST https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessToken` | string | no | Entity access token required by FCC for folder creation, sent in the accessToken header by the documented endpoint. |
| `entityId` | string | no | Unique entity ID. |
| `folderName` | string | no | Name of the new folder. |
| `format` | string | no | Response format. FCC documents json, jsonp, xml. |
| `parentFolderId` | string | no | Unique ID of the parent folder. |
| `serviceCode` | string | no | Entity service code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entity_folder_id": "string",
      "entity_id": "string",
      "folder_name": "Ava Chen",
      "folder_path": "string",
      "parent_folder_id": "string",
      "source_service_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity_folder_id` | string | Created entity folder identifier. |
| `entity_id` | string | FCC entity identifier. |
| `folder_name` | string | Created folder name. |
| `folder_path` | string | Created folder path. |
| `parent_folder_id` | string | Parent folder identifier. |
| `source_service_code` | string | FCC source service code. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `POST /api/manager/folder/create.{format}` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

