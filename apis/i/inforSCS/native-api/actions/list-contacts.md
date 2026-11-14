# List Contacts with Infor ReserveCloud SCS

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.reservecloud.com/gateway/request`
- **Official documentation:** [List Contacts](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://www.reservecloud.com/web/university/universityDocumentDownloadViewable/50237)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderByField` | query | `string` | no | Specify the field name by which the results are ordered. Defaults to unspecified. |
| `asc` | query | `boolean` | no | Specify ascending order or descending. Specify true or false. Defaults to true. |
| `filters` | query | `string` | no | Specify the uniqueId of a known record, a string field name, EQUAL_TO and a string value or a date field name, comparison operator and a date to filter the results. Operators: EQUAL_TO, NOT_EQUAL_TO, LESS_THAN, LESS_THAN_OR_EQUAL_TO, GREATER_THAN, GREATER_THAN_OR_EQUAL_TO Examples: filters=[['startDate','GREATER_THAN','07/01/2013'], ['startDate','LESS_THAN','12/31/2015']] filters=[['uniqueId','EQUAL_TO',' 8bd88078-ea60-438e8022-34b79ce26f08']] |
