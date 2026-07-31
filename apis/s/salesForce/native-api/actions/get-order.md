# Find Order by OrderNumber with Salesforce

Get the ID for a single Order object by its Order Number

## Endpoint

- **Method:** `GET`
- **Path:** `services/data/v61.0/query?q=SELECT+Id+FROM+Order+WHERE+Customer_PO__c=':orderNumber'`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderNumber` | path | `string` | yes | The number for the Order we want to get |
