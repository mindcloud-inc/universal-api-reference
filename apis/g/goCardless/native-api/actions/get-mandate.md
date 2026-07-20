# Get Mandate with GoCardless

Retrieves a single mandate from GoCardless.

## Endpoint

- **Method:** `GET`
- **Path:** `/mandates/:identity`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Get Mandate](https://developer.gocardless.com/api-reference/#mandates-get-a-single-mandate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identity` | path | `string` | yes | ID of the existing mandate to retrieve. |
