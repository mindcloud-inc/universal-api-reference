# List Offering Submissions with CoachAccountable

Retrieves offering submissions from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Offering Submissions](https://www.coachaccountable.com/APIDocs#Offering.getSubmissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | no | Filter Offering Submissions by Client. |
| `OfferingID` | body | `number` | no | Filter Offering Submissions by Offering. |
| `name` | body | `string` | no | Filter Offering Submissions by Offering by name, supports partial matching on prefix. |
| `dateFrom` | body | `date` | no | Set to restrict Offering Submissions returned to those at or after the provided value. |
| `dateTo` | body | `date` | no | Set to restrict Offering Submissions returned to those at or before the provided value. |
