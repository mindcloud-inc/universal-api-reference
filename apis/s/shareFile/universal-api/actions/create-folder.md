# ShareFile: Create Folder



```
POST https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "Name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "Name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The parent folder item identifier where the new folder should be created. |
| `Name` | string | yes | The name of the folder to create. |
| `Description` | string | no | An optional description for the folder. |
| `Zone` | object | no | An optional ShareFile zone object for the folder. |
| `ExpirationDate` | string | no | An optional ISO timestamp for folder expiration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AssociatedFolderTemplateID": "string",
      "BandwidthLimitInMB": 1,
      "CreationDate": "string",
      "CreatorFirstName": "Ava",
      "CreatorLastName": "Chen",
      "CreatorNameShort": "Ava Chen",
      "Description": "string",
      "DiskSpaceLimit": 1,
      "ExpirationDate": "string",
      "ExpirationDays": 1,
      "FileCount": 1,
      "FileName": "Ava Chen",
      "FileSizeBytes": 1,
      "FileSizeInKB": 1,
      "HasPendingAsyncOp": true,
      "HasPendingDeletion": true,
      "HasPermissionInfo": true,
      "Id": "string",
      "Info": {},
      "IsHidden": true,
      "IsTemplateOwned": true,
      "LastActivityUserNameShort": "Ava Chen",
      "LastModifiedByUserID": "string",
      "Name": "Ava Chen",
      "odata": {
        "metadata": "string",
        "type": "string"
      },
      "Parent": {},
      "Path": "string",
      "ProgenyEditDate": "string",
      "State": 1,
      "StreamID": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AssociatedFolderTemplateID` | string |  |
| `BandwidthLimitInMB` | number |  |
| `CreationDate` | string |  |
| `CreatorFirstName` | string |  |
| `CreatorLastName` | string |  |
| `CreatorNameShort` | string |  |
| `Description` | string |  |
| `DiskSpaceLimit` | number |  |
| `ExpirationDate` | string |  |
| `ExpirationDays` | number |  |
| `FileCount` | number |  |
| `FileName` | string |  |
| `FileSizeBytes` | number |  |
| `FileSizeInKB` | number |  |
| `HasPendingAsyncOp` | boolean |  |
| `HasPendingDeletion` | boolean |  |
| `HasPermissionInfo` | boolean |  |
| `Id` | string |  |
| `Info` | object |  |
| `IsHidden` | boolean |  |
| `IsTemplateOwned` | boolean |  |
| `LastActivityUserNameShort` | string |  |
| `LastModifiedByUserID` | string |  |
| `Name` | string |  |
| `odata.metadata` | string |  |
| `odata.type` | string |  |
| `Parent` | object |  |
| `Path` | string |  |
| `ProgenyEditDate` | string |  |
| `State` | number |  |
| `StreamID` | string |  |
| `url` | string |  |

## Native endpoint

Through the native ShareFile API, this operation is `POST /Items({{id}})/Folder` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

