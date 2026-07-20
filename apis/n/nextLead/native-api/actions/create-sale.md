# Create Sale with NextLead

Creates a new sales deal in NextLead.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/receive/sales/create-sale`
- **Base URL:** `https://dashboard.nextlead.app`
- **Official documentation:** [Create Sale](https://dashboard.nextlead.app/en/api-documentation#receive-sale-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Sale name. |
| `column` | body | `string` | yes | Sales column identifier. |
