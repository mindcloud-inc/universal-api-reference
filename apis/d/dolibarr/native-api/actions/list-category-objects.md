# List Category Objects with Dolibarr

Retrieves objects from a Dolibarr category.

## Endpoint

- **Method:** `GET`
- **Path:** `/categories/{id}/objects`
- **Base URL:** `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`
- **Official documentation:** [List Category Objects](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Dolibarr category ID. |
