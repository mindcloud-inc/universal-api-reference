# List Badge Assertions with Navigatr

## Endpoint

- **Method:** `GET`
- **Path:** `/badge_assertion/`
- **Base URL:** `https://api.navigatr.app/v1`
- **Official documentation:** [List Badge Assertions](https://api.navigatr.app/docs#/Badge%20Assertion/badge_assertion_read_badge_assertions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipient_id` | query | `number` | no | Retrieve assertions issued to a specific user. Use `0` for the current user, or `19524` for the known Navigatr test user when a concrete ID is needed. |
| `badge_id` | query | `number` | no | Retrieve assertions for a specific badge. |
| `provider_id` | query | `number` | no | Retrieve assertions issued by a specific provider. |
| `recipient_email` | query | `string` | no | Retrieve assertions issued to a specific email address. The docs note this filter is typically admin-only. |
| `order_by` | query | `string` | no | Order results by newest first by default, or by badge name / time created using the provider-supported values. |
| `keyword` | query | `string` | no | Filter badge assertions by badge names similar to the provided text. |
| `status` | query | `string` | no | Filter by one or more badge assertion statuses as a comma-separated string, such as `Pending,Claimed`. |
