# Connect Person to Opportunity with OneSuite

Connects a person to an opportunity in OneSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people/:people_id/opportunity`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Connect Person to Opportunity](https://rest-api.onesuite.io/#connect-people-to-opportunity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `people_id` | path | `string` | yes | People ID from the connect-people-to-opportunity docs. |
| `opportunityId` | body | `string` | yes | Opportunity ID to connect to the person. |
