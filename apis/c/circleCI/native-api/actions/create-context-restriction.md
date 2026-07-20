# Create Context Restriction with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/context/:context_id/restrictions`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Create Context Restriction](https://circleci.com/docs/api/v2/#tag/Context-Restrictions/operation/createContextRestriction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `restriction_type` | body | `string` | yes | Restriction type: project, expression, or group. |
| `restriction_value` | body | `string` | yes | Restriction value for the chosen restriction type. |
