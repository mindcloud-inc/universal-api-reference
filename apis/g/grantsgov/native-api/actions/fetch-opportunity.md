# Fetch Opportunity with Grants.gov

Retrieves grant opportunity details from Grants.gov by opportunity ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/api/fetchOpportunity`
- **Base URL:** `https://api.grants.gov`
- **Official documentation:** [Fetch Opportunity](https://grants.gov/api/common/fetchopportunity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunityId` | body | `number` | yes | Numeric Grants.gov opportunity identifier returned by Search Opportunities. |
