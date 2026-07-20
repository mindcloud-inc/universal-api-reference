# PrivacyManager anonymize Some Raw Data with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [PrivacyManager anonymize Some Raw Data](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSites` | body | `string` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `anonymizeIp` | body | `string` | no | Matomo API parameter. |
| `anonymizeLocation` | body | `string` | no | Matomo API parameter. |
| `anonymizeUserId` | body | `string` | no | Matomo API parameter. |
| `unsetVisitColumns` | body | `string` | no | Matomo API parameter. |
| `unsetLinkVisitActionColumns` | body | `string` | no | Matomo API parameter. |
| `passwordConfirmation` | body | `string` | no | Matomo API parameter. |
