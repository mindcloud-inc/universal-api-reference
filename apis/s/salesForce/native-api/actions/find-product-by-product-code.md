# Find Product Offer by Product Code with Salesforce

## Endpoint

- **Method:** `GET`
- **Path:** `services/data/v61.0/query?q=SELECT+Id,+ProductCode,+UPC__c,+%28SELECT+Quantity__c,+Consumed_Quantity__c,+id,+Vendor_ID__c,+Vendor_Offer__c+FROM Offers__r%29+FROM+Product2+WHERE+ProductCode+=+':productcode'`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `productcode` | path | `string` | no |
