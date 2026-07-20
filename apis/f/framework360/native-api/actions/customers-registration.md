# Register Customer with Framework360

## Endpoint

- **Method:** `POST`
- **Path:** `customers/registration`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [Register Customer](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nome` | body | `string` | yes | Customer first name. |
| `cognome` | body | `string` | yes | Customer last name. |
| `email` | body | `string` | yes | Customer email address. |
| `password` | body | `string` | yes | Customer password. |
| `telefono` | body | `string` | no | Customer phone number. |
| `provenienza` | body | `number` | no | Customer source ID. |
| `dati_fatturazione` | body | `object` | no | Billing profile data for the customer. |
| `marketing_list[]` | body | `array<number>` | no | Marketing lists to subscribe the customer to. |
| `marketing_active` | body | `boolean` | no | Whether marketing is active for the customer. |
| `tags[]` | body | `array<string>` | no | Tags to assign to the customer. |
| `extraFields` | body | `object` | no | Custom extra fields for the customer profile. |
| `cart[]` | body | `array<object>` | no | Cart associated with the customer. |
