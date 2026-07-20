# Update User Onboarding with RotaCloud

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/users/onboard/:id`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update User Onboarding](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Onboarding user ID. |
| `title` | body | `string` | yes | User title. |
| `gender` | body | `string` | yes | User gender. |
| `dob` | body | `string` | yes | Date of birth in YYYY-MM-DD format. |
| `nationalInsuranceNumber` | body | `string` | no | National insurance number. |
| `address1` | body | `string` | yes | Primary address line. |
| `address2` | body | `string` | yes | Secondary address line. |
| `county` | body | `string` | yes | County or state. |
| `phone` | body | `string` | yes | Phone number. |
| `postcode` | body | `string` | yes | Postal code. |
| `city` | body | `string` | yes | City. |
| `emergencyContactName` | body | `string` | yes | Emergency contact name. |
| `emergencyContactPhone` | body | `string` | yes | Emergency contact phone. |
| `emergencyContactRelationship` | body | `string` | yes | Emergency contact relationship. |
