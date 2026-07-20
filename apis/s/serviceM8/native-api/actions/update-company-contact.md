# Update Company Contact with ServiceM8

## Endpoint

- **Method:** `POST`
- **Path:** `/api_1.0/companycontact/:uuid.json`
- **Base URL:** `https://api.servicem8.com`
- **Official documentation:** [Update Company Contact](https://developer.servicem8.com/reference/updatecompanycontacts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `uuid` | path | `string` | yes |
| `company_uuid` | body | `string` | no |
| `first` | body | `string` | no |
| `last` | body | `string` | no |
| `phone` | body | `string` | no |
| `mobile` | body | `string` | no |
| `email` | body | `string` | no |
| `type` | body | `string` | no |
| `is_primary_contact` | body | `boolean` | no |
