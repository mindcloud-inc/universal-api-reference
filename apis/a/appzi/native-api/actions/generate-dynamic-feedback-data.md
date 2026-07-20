# Generate Dynamic Feedback Data with Appzi

Generates Appzi dynamic feedback data settings.

## Endpoint

- **Method:** `GET`
- **Path:** `https://docs.appzi.io/integration/add-data/`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Generate Dynamic Feedback Data](https://docs.appzi.io/integration/add-data/#dynamic-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userAccessor` | query | `string` | no | Optional expression that returns the current user object. |
| `userIdExpression` | query | `string` | no | Optional expression used for the userId field. |
| `planExpression` | query | `string` | no | Optional expression used for the plan field. |
| `createdAtExpression` | query | `string` | no | Optional expression used for the accountCreated value. |
