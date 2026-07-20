# Microsoft Power BI: Post Import



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/imports-post-import
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/imports-post-import" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetDisplayName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/imports-post-import', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetDisplayName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetDisplayName` | string | yes | The display name of the dataset, should include file extension. Not supported when importing from OneDrive for Business. |
| `nameConflict` | object | no | Specifies what to do if a dataset with the same name already exists. The default value is Ignore. For RDL files, Abort and Overwrite are the only supported options and not others. |
| `overrideModelLabel` | boolean | no | Whether to override the existing label on a model when republishing a Power BI .pbix file. The service default value is true. |
| `overrideReportLabel` | boolean | no | Whether to override the existing report label when republishing a Power BI .pbix file. The service default value is true. |
| `skipReport` | boolean | no | Whether to skip report import. If specified, the value must be true. Only supported for Power BI .pbix files. |
| `subfolderObjectId` | string | no | The subfolder ID to import the file to subfolder. |
| `connectionType` | object | no | The import connection type for a OneDrive for Business file |
| `filePath` | string | no | The path of the OneDrive for Business Excel (.xlsx) file to import, which can be absolute or relative. Power BI .pbix files aren't supported. |
| `fileUrl` | string | no | The shared access signature URL of the temporary blob storage used to import large Power BI .pbix files between 1 GB and 10 GB in size. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST imports` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/imports-post-import.md) for the provider-specific parameters and requirements.

