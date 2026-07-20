# Update Affiliate with Xola

Updates an existing affiliate in Xola.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sellers/{id}/affiliates`
- **Base URL:** `https://sandbox.xola.com/api`
- **Official documentation:** [Update Affiliate](https://developers.xola.com/reference/update-an-affiliate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | — |
| `id` | path | `string` | yes | Seller identifier from Xola. |
| `name` | body | `string` | yes | — |
