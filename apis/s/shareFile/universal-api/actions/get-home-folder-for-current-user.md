# ShareFile: Get Home Folder for Current User



```
GET https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-home-folder-for-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-home-folder-for-current-user?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-home-folder-for-current-user?${params}`, {
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
| `AssociatedFolderTemplateID` | string | The associated folder template identifier. |
| `BandwidthLimitInMB` | number | The bandwidth limit for the item. |
| `CreationDate` | string | The item creation timestamp. |
| `CreatorFirstName` | string | The creator first name. |
| `CreatorLastName` | string | The creator last name. |
| `CreatorNameShort` | string | The creator short display name. |
| `Description` | string | The item description. |
| `DiskSpaceLimit` | number | The disk space limit for the item. |
| `ExpirationDate` | string | The item expiration timestamp. |
| `ExpirationDays` | number | The remaining expiration days. |
| `FileCount` | number | The number of files directly under the returned root item. |
| `FileName` | string | The underlying file or folder name. |
| `FileSizeBytes` | number | The item size in bytes. |
| `FileSizeInKB` | number | The item size in kilobytes. |
| `HasPendingAsyncOp` | boolean | Whether an async operation is pending. |
| `HasPendingDeletion` | boolean | Whether the item has a pending deletion. |
| `HasPermissionInfo` | boolean | Whether permission information is present. |
| `Id` | string | The ShareFile item identifier. |
| `Info` | object | Capability and folder metadata for the returned item. |
| `IsHidden` | boolean | Whether the item is hidden. |
| `IsTemplateOwned` | boolean | Whether the template is owned by the current user. |
| `LastModifiedByUserID` | string | The user identifier that last modified the item. |
| `Name` | string | The item display name. |
| `odata.metadata` | string | The OData metadata URL for the returned item. |
| `odata.type` | string | The OData type for the returned item. |
| `Parent` | object | The parent item reference. |
| `Path` | string | The item path. |
| `ProgenyEditDate` | string | The last descendant edit timestamp. |
| `State` | number | The ShareFile state code. |
| `StreamID` | string | The ShareFile stream identifier. |
| `url` | string | The API URL for the returned item. |

## Native endpoint

Through the native ShareFile API, this operation is `GET /Items` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-home-folder-for-current-user.md) for the provider-specific parameters and requirements.

