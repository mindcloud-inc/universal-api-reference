# Get User By Email with Dolibarr

Retrieves a user from Dolibarr by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/email/{email}`
- **Base URL:** `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`
- **Official documentation:** [Get User By Email](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Dolibarr user email address. |
