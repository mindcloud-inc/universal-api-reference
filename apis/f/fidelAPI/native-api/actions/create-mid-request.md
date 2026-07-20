# Create MID Request with Fidel API

Creates a MID request in Fidel API.

## Endpoint

- **Method:** `POST`
- **Path:** `/programs/:programId/mid-requests`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Create MID Request](https://docs.fidelapi.com/docs/select/mid-management#mid-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | path | `string` | yes | — |
| `action` | body | `string` | yes | MID request action. |
| `locationId` | body | `string` | yes | The location where the MID should be onboarded. |
| `scheme` | body | `string` | yes | Card scheme for the MID request. |
| `origin` | body | `string` | yes | Source of the MID. |
| `visaAcquiringMid` | body | `string` | yes | Visa acquiring MID for brand-provided or processor-provided Visa onboarding. |
| `visaBin` | body | `string` | yes | Visa BIN for Visa onboarding. |
