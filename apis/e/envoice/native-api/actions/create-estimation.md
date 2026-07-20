# Create Estimation with Envoice

Creates a new estimation in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `estimation/new`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Create Estimation](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientId` | body | `number` | yes | Client identifier for the estimation. |
| `CurrencyId` | body | `number` | yes | Currency identifier. |
| `ExpiresOn` | body | `date` | yes | Estimation expiration date. |
| `IssuedOn` | body | `date` | yes | Estimation issue date. |
| `Items` | body | `string` | yes | JSON array of estimation item objects. |
| `Notes` | body | `string` | no | Internal estimation notes. |
| `Number` | body | `string` | yes | Unique estimation number. |
| `PaymentGateways` | body | `string` | no | JSON array of estimation payment gateway objects. |
| `Status` | body | `string` | yes | Estimation status. |
| `Terms` | body | `string` | no | Estimation terms. |
