# Create Payment with VSCO Workspace

Creates a new payment in VSCO Workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment`
- **Base URL:** `https://workspace.vsco.co/api/v2`
- **Official documentation:** [Create Payment](https://workspace.vsco.co/api/#operation/createResourcePayment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | body | `string` | yes | A ULID entity identifier that is nullable. |
| `payerId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `paymentMethodId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `invoiceItemId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `status` | body | `string` | no | — |
| `amount` | body | `number` | yes | — |
| `memo` | body | `string` | no | — |
| `checkNumber` | body | `string` | no | — |
| `transactionId` | body | `string` | no | — |
| `authCode` | body | `string` | no | — |
| `received` | body | `date` | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
