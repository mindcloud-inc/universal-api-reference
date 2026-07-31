# Update Product with Salesforce

## Endpoint

- **Method:** `PATCH`
- **Path:** `/services/data/v64.0/sobjects/Product2/:id`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`
- **Official documentation:** [Update Product](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_product2.htm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Description` | body | `string` | no |
| `IsActive` | body | `boolean` | no |
| `ProductCode` | body | `string` | no |
| `Name` | body | `string` | no |
| `id` | path | `string` | no |
