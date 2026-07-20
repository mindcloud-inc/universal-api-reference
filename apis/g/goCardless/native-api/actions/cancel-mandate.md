# Cancel Mandate with GoCardless

Cancels an existing mandate in GoCardless.

## Endpoint

- **Method:** `POST`
- **Path:** `/mandates/:identity/actions/cancel`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Cancel Mandate](https://developer.gocardless.com/api-reference/#mandates-cancel-a-mandate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identity` | path | `string` | yes | ID of the mandate to cancel. |
| `metadata` | body | `object` | no | Optional metadata stored on the mandate cancellation event. |
