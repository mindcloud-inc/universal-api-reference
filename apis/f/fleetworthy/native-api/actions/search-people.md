# Search People with Fleetworthy

## Endpoint

- **Method:** `POST`
- **Path:** `/people-bulk/search`
- **Base URL:** `https://apis.fleetworthy.com/compliance-api/v1`
- **Official documentation:** [Search People](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=post-people-bulk-search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stringSearch` | body | `string` | no | Search by a person's identifying text. |
| `entitySearch[]` | body | `array<string>` | no | Limit the search to Fleetworthy location IDs. |
| `isActive` | body | `boolean` | no | Return active people when enabled. |
| `advancedFilter` | body | `object` | no | Optional Fleetworthy person filter object, such as firstName, lastName, email, or SocialSecurityNumberLastFour. |
