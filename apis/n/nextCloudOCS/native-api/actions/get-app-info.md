# Get App Info with Next Cloud OCS

Retrieves app details from Next Cloud OCS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ocs/v1.php/cloud/apps/{{appId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Get App Info](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_apps.html#get-app-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Nextcloud app ID, for example files. |
