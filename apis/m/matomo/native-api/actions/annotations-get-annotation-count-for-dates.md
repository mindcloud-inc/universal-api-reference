# Annotations get Annotation Count For Dates with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [Annotations get Annotation Count For Dates](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `period` | body | `string` | yes | Matomo API parameter. |
| `?int lastN` | body | `string` | yes | Matomo API parameter. |
| `getAnnotationText` | body | `string` | no | Matomo API parameter. |
