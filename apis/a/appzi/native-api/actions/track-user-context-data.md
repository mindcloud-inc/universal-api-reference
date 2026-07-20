# Track User Context Data with Appzi

Generates Appzi user context tracking settings.

## Endpoint

- **Method:** `GET`
- **Path:** `https://docs.appzi.io/integration/add-data/`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Track User Context Data](https://docs.appzi.io/integration/add-data/#track-user-context)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | query | `string` | yes | The user identifier to include in the Appzi tracking payload. |
| `subscriptionPlan` | query | `string` | no | Optional subscription or plan label to include as contextual metadata. |
| `accountAge` | query | `string` | no | Optional account-age label to include for segmentation context. |
