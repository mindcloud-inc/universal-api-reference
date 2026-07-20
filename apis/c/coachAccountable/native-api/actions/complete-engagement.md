# Complete Engagement with CoachAccountable

Completes an engagement in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Complete Engagement](https://www.coachaccountable.com/APIDocs#Engagement.complete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EngagementID` | body | `number` | yes | — |
| `whenOption` | body | `list` | no | When should the Engagement be noted as having been completed? Accepted values: `E`, `N`, `U`. |
