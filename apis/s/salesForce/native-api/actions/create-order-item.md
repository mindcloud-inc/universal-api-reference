# Create Order Item with Salesforce

## Endpoint

- **Method:** `POST`
- **Path:** `/services/data/v64.0/sobjects/OrderItem`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`
- **Official documentation:** [Create Order Item](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_orderitem.htm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `product2Id` | body | `string` | yes |
| `quantity` | body | `string` | no |
| `orderId` | body | `string` | yes |
| `unitPrice` | body | `string` | no |
| `listPrice` | body | `string` | no |
| `pricebookEntryId` | body | `string` | no |
