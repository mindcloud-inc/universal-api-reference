# Update Invoice Category with Envoice

Updates an existing invoice category in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `invoice/updatecategory`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Update Invoice Category](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `number` | yes | Invoice category identifier. |
| `Name` | body | `string` | yes | Invoice category name. |
