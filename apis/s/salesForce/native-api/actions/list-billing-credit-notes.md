# List Billing Credit Notes with Salesforce

## Endpoint

- **Method:** `GET`
- **Path:** `/services/data/v61.0/query`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`
- **API:** REST SOQL Read
- **Official documentation:** [List Billing Credit Notes](https://developer.salesforce.com/docs/platform/api-rest/guide/resources-query)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list<string>` | no | Match the current blng__Status__c value exactly. This does not detect a transition into that status. Accepted values: `Cancelled`, `Draft`, `Posted`. |
