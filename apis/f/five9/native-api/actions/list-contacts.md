# List Contacts with Five9

## Endpoint

- **Method:** `GET`
- **Path:** `https://app-scl.five9.com/appsvcs/rs/svc/orgs/:domainID/getContactRecords`
- **Base URL:** `https://api.prod.us.five9.net/acl/v1/`
- **Official documentation:** [List Contacts](https://documentation.five9.com/bundle/admin-console/page/admin-console/contact-fields/_ch-contact-fields.htm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | no |
| `lastName` | body | `string` | no |
| `phoneNumber` | body | `string` | no |
| `firstName` | body | `string` | no |
| `domainID` | path | `string` | yes |
