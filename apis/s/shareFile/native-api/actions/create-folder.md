# Create Folder with ShareFile

## Endpoint

- **Method:** `POST`
- **Path:** `/Items({{id}})/Folder`
- **Base URL:** `https://{subdomain}.{apicp}/sf/v3`
- **Official documentation:** [Create Folder](https://api.sharefile.com/html/docs/Items.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The parent folder item identifier where the new folder should be created. |
| `Name` | body | `string` | yes | The name of the folder to create. |
| `Description` | body | `string` | no | An optional description for the folder. |
| `Zone` | body | `object` | no | An optional ShareFile zone object for the folder. |
| `ExpirationDate` | body | `string` | no | An optional ISO timestamp for folder expiration. |
