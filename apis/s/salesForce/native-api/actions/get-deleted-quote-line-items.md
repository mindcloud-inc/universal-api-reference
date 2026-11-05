# Get Deleted Quote Line Items with Salesforce

## Endpoint

- **Method:** `GET`
- **Path:** `/services/data/v61.0/sobjects/QuoteLineItem/deleted/`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`
- **API:** REST Deleted Records Read
- **Official documentation:** [Get Deleted Quote Line Items](https://developer.salesforce.com/docs/platform/api-rest/guide/resources-getdeleted.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `date` | yes | UTC timestamp. Salesforce ignores seconds and only retains recent deletion coverage (up to 15 days). |
| `end` | query | `date` | yes | UTC timestamp. Salesforce ignores seconds and only retains recent deletion coverage (up to 15 days). |
