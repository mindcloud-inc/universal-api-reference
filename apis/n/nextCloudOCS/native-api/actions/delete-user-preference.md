# Delete User Preference with Next Cloud OCS

Deletes a user preference from Next Cloud OCS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/ocs/v2.php/apps/provisioning_api/api/v1/config/users/{{preferenceAppId}}/{{configKey}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Delete User Preference](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-user-preferences-api.html#deleting-a-preference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configKey` | path | `string` | yes | Preference key. |
| `preferenceAppId` | path | `string` | yes | Nextcloud preference namespace app ID. |
