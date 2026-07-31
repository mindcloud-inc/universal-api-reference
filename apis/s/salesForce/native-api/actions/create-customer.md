# Create Customer with Salesforce

## Endpoint

- **Method:** `POST`
- **Path:** `services/data/v62.0/sobjects/Contact`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`
- **Official documentation:** [Create Customer](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_contact.htm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `FirstName` | body | `string` | no |
| `LastName` | body | `string` | yes |
| `Phone` | body | `string` | no |
| `Email` | body | `string` | no |
| `accountId` | body | `string` | yes |
| `ownerId` | body | `string` | yes |
