# Resend Donation Receipt with Raisely

Resends a donation receipt from Raisely.

## Endpoint

- **Method:** `POST`
- **Path:** `/donations/:uuid/resend`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Resend Donation Receipt](https://developers.raisely.com/reference/postdonationsresend)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | The `uuid` of the record |
| `data` | body | `object` | no | — |
| `email` | body | `string` | no | Optional email to send the receipt to (defaults to the email on the donation) |
