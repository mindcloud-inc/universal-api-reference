# Query Order Items (test) with Salesforce

## Endpoint

- **Method:** `GET`
- **Path:** `services/data/v61.0/query`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `advancedOptions.orderBy` | query | `list<string>` | no | — |
| `where` | query | `string` | yes | This is a SOQL WHERE clause. Example: "AccountType != 'Vendor' AND CreatedDate != TODAY". Read more. |
| `advancedOptions.orderByDirection` | query | `list<string>` | no | Order Direction (ASC or DESC) - defaults is DESC. |
| `select` | query | `list<string>` | no | Choose the fields to display in the response for this action. Send multiple values as a array. |
| `advancedOptions.limit` | query | `number` | no | Specify the limit for records returned in the response. The # of results. Example: 10. (Default: 2000) |
| `advancedOptions` | query | `object` | no | Specify additional query parameters and advanced SOQL syntax below. |
