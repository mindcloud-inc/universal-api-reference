# Change Estimation Status with Envoice

Updates an estimation status in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `estimation/changestatus`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Change Estimation Status](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `number` | yes | Estimation identifier. |
| `Status` | body | `string` | yes | New estimation status: Draft, Accepted, or Rejected. |
