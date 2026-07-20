# Get Country By Code with Dolibarr

Retrieves a country from Dolibarr by code.

## Endpoint

- **Method:** `GET`
- **Path:** `/setup/dictionary/countries/byCode/{code}`
- **Base URL:** `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`
- **Official documentation:** [Get Country By Code](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Dolibarr country code. |
