# Delete User Preferences with Next Cloud OCS

Deletes user preferences from Next Cloud OCS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/ocs/v2.php/apps/provisioning_api/api/v1/config/users/{{preferenceAppId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Delete User Preferences](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-user-preferences-api.html#deleting-multiple-preference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configKeys` | body | `list<string>` | yes | List of preference keys to delete. |
| `preferenceAppId` | path | `string` | yes | Nextcloud preference namespace app ID. |
