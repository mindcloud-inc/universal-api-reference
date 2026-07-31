# Update Order Items with Salesforce

## Endpoint

- **Method:** `PATCH`
- **Path:** `services/data/v61.0/sobjects/OrderItem/:id`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | no |
| `Vendor_Invoice_Number__c` | body | `string` | no |
| `Carrier__c` | body | `string` | no |
| `Tracking_Number__c` | body | `string` | no |
| `Service_Type__c` | body | `string` | no |
| `Product_Status__c` | body | `string` | no |
| `Synced__c` | body | `boolean` | no |
