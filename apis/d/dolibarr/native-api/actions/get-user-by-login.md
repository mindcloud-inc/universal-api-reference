# Get User By Login with Dolibarr

Retrieves a user from Dolibarr by login.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/login/{login}`
- **Base URL:** `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`
- **Official documentation:** [Get User By Login](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `login` | path | `string` | yes | Dolibarr user login. |
