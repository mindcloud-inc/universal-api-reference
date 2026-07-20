# List Context Restrictions with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/context/:context_id/restrictions`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Context Restrictions](https://circleci.com/docs/api/v2/#tag/Context-Restrictions/operation/getContextRestrictions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `context_id` | path | `string` | no | The CircleCI context UUID. |
