# Enable App with Next Cloud OCS

Enables an app in Next Cloud OCS.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocs/v1.php/cloud/apps/{{appId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Enable App](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_apps.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Nextcloud app ID. |
