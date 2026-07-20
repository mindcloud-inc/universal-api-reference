# Get Plan Limits By Version with Pinghome

Retrieves plan limits from Pinghome by version.

## Endpoint

- **Method:** `GET`
- **Path:** `https://customer-query.api.pinghome.io/v1/plan/:plan/:version/limits`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Get Plan Limits By Version](https://docs.pinghome.io/billing-operations-management/get-plan-limits-by-version/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `plan` | path | `string` | yes | The plan identifier, such as team, developer, or business. |
| `version` | path | `string` | yes | The plan version identifier, for example v1. |
