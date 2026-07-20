# List Object Categories with Dolibarr

Retrieves categories for an object in Dolibarr.

## Endpoint

- **Method:** `GET`
- **Path:** `/categories/object/{type}/{id}`
- **Base URL:** `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`
- **Official documentation:** [List Object Categories](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Dolibarr object ID associated with the category. |
| `type` | path | `string` | yes | Dolibarr object type associated with the category. |
