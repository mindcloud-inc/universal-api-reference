# Get Country By ISO with Dolibarr

Retrieves a country from Dolibarr by ISO code.

## Endpoint

- **Method:** `GET`
- **Path:** `/setup/dictionary/countries/byISO/{iso}`
- **Base URL:** `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`
- **Official documentation:** [Get Country By ISO](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `iso` | path | `string` | yes | Dolibarr country ISO code. |
