# Set User Preferences with Next Cloud OCS

Sets user preferences in Next Cloud OCS.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocs/v2.php/apps/provisioning_api/api/v1/config/users/{{preferenceAppId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Set User Preferences](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-user-preferences-api.html#setting-multiple-preference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `config` | body | `object` | yes | Key-value preference object. |
| `preferenceAppId` | path | `string` | yes | Nextcloud preference namespace app ID. |
