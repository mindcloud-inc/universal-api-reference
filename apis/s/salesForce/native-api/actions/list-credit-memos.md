# List Credit Memos with Salesforce

## Endpoint

- **Method:** `GET`
- **Path:** `/services/data/v61.0/query`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`
- **API:** REST SOQL Read
- **Official documentation:** [List Credit Memos](https://developer.salesforce.com/docs/platform/api-rest/guide/resources-query)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Match the current Status value exactly. This does not detect a transition into that status. |
