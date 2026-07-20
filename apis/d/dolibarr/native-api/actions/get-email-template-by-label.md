# Get Email Template By Label with Dolibarr

Retrieves an email template from Dolibarr by label.

## Endpoint

- **Method:** `GET`
- **Path:** `/emailtemplates/label/{label}`
- **Base URL:** `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`
- **Official documentation:** [Get Email Template By Label](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer))

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | path | `string` | yes | Dolibarr email template label. |
