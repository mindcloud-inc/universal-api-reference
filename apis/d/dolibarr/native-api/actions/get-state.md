# Get State with Dolibarr

Retrieves a state or province from Dolibarr.

## Endpoint

- **Method:** `GET`
- **Path:** `/setup/dictionary/states/{id}`
- **Base URL:** `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`
- **Official documentation:** [Get State](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Dolibarr state or province ID. |
