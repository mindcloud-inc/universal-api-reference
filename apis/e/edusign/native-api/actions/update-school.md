# Update School with Edusign

Updates your school details in Edusign.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/school`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Update School](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `school` | body | `object` | yes | — |
| `school.NAME` | body | `string` | yes | School name |
| `school.LOGO` | body | `string` | yes | School logo |
| `school.LOGOS[]` | body | `array<object>` | no | — |
| `school.LOGOS[]` | body | `array<object>` | no | — |
| `school.LOGOS[]` | body | `array<object>` | no | — |
| `school.STREET_ADDRESS` | body | `string` | yes | School street address |
| `school.CITY` | body | `string` | yes | School city |
| `school.POSTALCODE` | body | `string` | yes | School postal code |
| `school.COUNTRY` | body | `string` | yes | School country |
| `school.PHONE` | body | `string` | yes | School phone |
| `school.WEBHOOKS[]` | body | `array<object>` | no | — |
| `school.WEBHOOKS[]` | body | `array<object>` | no | — |
| `school.WEBHOOKS[]` | body | `array<object>` | no | — |
