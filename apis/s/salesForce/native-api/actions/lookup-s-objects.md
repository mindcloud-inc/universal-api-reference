# Org sObjects (Lookup) with Salesforce

Returns the authenticated organizations sObjects for Lookup fields.

## Endpoint

- **Method:** `GET`
- **Path:** `services/data/v61.0/sobjects/`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`
- **Official documentation:** [Org sObjects (Lookup)](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_sobject_describe.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `list<string>` | no | Accepted values: `all`, `createable`, `custom`, `queryable`, `searchable`, `updateable`. Send multiple values as a array. |
