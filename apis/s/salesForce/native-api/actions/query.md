# Query (SOQL) with Salesforce

Use raw SOQL syntax to Query your Salesforce Org.

## Endpoint

- **Method:** `GET`
- **Path:** `services/data/:apiVersion/query`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`
- **API:** REST
- **Official documentation:** [Query (SOQL)](https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql_select.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | — |
| `apiVersion` | path | `string` | no | Salesforce REST API version for this query, including the v prefix (for example, v66.0). Defaults to v61.0 to preserve existing Query behavior. DebitMemo requires v65.0 or later and the appropriate Revenue Cloud Billing license and permissions. |
