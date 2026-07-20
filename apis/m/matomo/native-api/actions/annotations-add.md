# Annotations add with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [Annotations add](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `note` | body | `string` | yes | Matomo API parameter. |
| `starred` | body | `string` | no | Matomo API parameter. |
