# List Verifications with Vouchsafe

Retrieves a list of verifications from Vouchsafe.

## Endpoint

- **Method:** `GET`
- **Path:** `/verifications`
- **Base URL:** `https://app.vouchsafe.id/api/v1`
- **Official documentation:** [List Verifications](https://app.vouchsafe.id/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list` | no | Optional status filter. Accepted values: `Blocked`, `Cancelled`, `InProgress`, `LockedOut`, `ManuallyReviewed`, `ReadyForReview`, `Refused`, `Verified`. |
