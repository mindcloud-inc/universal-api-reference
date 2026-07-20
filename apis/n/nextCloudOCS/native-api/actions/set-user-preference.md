# Set User Preference with Next Cloud OCS

Sets a user preference in Next Cloud OCS.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocs/v2.php/apps/provisioning_api/api/v1/config/users/{{preferenceAppId}}/{{configKey}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Set User Preference](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-user-preferences-api.html#setting-a-preference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configKey` | path | `string` | yes | Preference key. |
| `configValue` | body | `string` | yes | Preference value to save. |
| `preferenceAppId` | path | `string` | yes | Nextcloud preference namespace app ID. |
