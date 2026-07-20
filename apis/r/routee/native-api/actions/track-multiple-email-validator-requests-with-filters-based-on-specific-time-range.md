# Track multiple Email Validator requests with filters based on specific time range with Routee

Tracks multiple email validator requests with filters based on specific time range in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/emailvalidator/tracking`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Track multiple Email Validator requests with filters based on specific time range](https://docs.routee.net/reference/track-multiple-email-validator-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateStart` | query | `string` | yes | ISO-8601 date-time format. |
| `dateEnd` | query | `string` | yes | ISO-8601 date-time format. |
| `page` | query | `string` | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | query | `string` | no | The number of items to retrieve, default value is 20. Max value is 2000. |
| `fieldName` | body | `string` | yes | The name of the field to apply the filtering. Available values: email, exists, trackingId, hasValidFormat, hasValidDNS, label, |
| `searchTerm` | body | `string` | yes | The exact value that the specified field must match. |
| `searchOperator` | body | `string` | yes | The operator upon which the search operation will be executed. Possible values: 'IS', 'IS_NOT', 'CONTAINS', 'STARTS_WITH', 'ENDS_WITH'. |
