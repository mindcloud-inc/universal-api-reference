# Create Account with Salesforce

## Endpoint

- **Method:** `POST`
- **Path:** `services/data/v62.0/sobjects/Account`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`
- **Official documentation:** [Create Account](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_account.htm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `ownerId` | body | `string` | yes |
| `billingStreet` | body | `string` | no |
| `billingCity` | body | `string` | no |
| `billingState` | body | `string` | no |
| `billingPostalCode` | body | `string` | no |
| `billingCountry` | body | `string` | no |
| `website` | body | `string` | no |
