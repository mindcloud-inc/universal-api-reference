# Query (SOQL) with Salesforce

Use raw SOQL syntax to Query your Salesforce Org.

## Endpoint

- **Method:** `GET`
- **Path:** `services/data/v61.0/query`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`
- **Official documentation:** [Query (SOQL)](https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql_select.htm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `q` | query | `string` | yes |
