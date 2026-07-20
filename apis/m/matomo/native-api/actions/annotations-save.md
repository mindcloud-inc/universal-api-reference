# Annotations save with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [Annotations save](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `idNote` | body | `string` | yes | Matomo API parameter. |
| `?string date` | body | `string` | yes | Matomo API parameter. |
| `?string note` | body | `string` | yes | Matomo API parameter. |
| `?bool starred` | body | `string` | yes | Matomo API parameter. |
