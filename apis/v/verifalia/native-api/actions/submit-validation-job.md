# Submit Validation Job with Verifalia

Creates a new email validation job in Verifalia.

## Endpoint

- **Method:** `POST`
- **Path:** `/email-validations`
- **Base URL:** `https://api-1.verifalia.com/v2.7`
- **Official documentation:** [Submit Validation Job](https://verifalia.com/developers/email-verifications/creating-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `waitTime` | query | `number` | no | Milliseconds to wait for job completion before Verifalia returns immediately. Valid range: 0 to 30000. |
