# Create Affiliate with Xola

Creates a new affiliate for a seller in Xola.

## Endpoint

- **Method:** `POST`
- **Path:** `/sellers/{id}/affiliates`
- **Base URL:** `https://sandbox.xola.com/api`
- **Official documentation:** [Create Affiliate](https://developers.xola.com/reference/create-an-affiliate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | — |
| `id` | path | `string` | yes | Seller identifier from Xola. |
| `name` | body | `string` | yes | — |
