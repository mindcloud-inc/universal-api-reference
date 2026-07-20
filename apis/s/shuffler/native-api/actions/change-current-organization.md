# Change Current Organization with Shuffler

Updates the current organization in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/{orgId}/change`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Change Current Organization](https://shuffler.io/docs/API#change-current-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | body | `string` | yes | Organization to switch to. |
| `orgId` | path | `string` | yes | Org Id path parameter. |
