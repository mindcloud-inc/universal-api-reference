# Update Invoice Template with Sonderplan

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoice-template`
- **Base URL:** `https://api.sonderplan.com/v2`
- **Official documentation:** [Update Invoice Template](https://docs.sonderplan.com/api-reference/invoice-template/update-invoice-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Invoice template payload. |
| `id` | query | `string` | yes | Invoice template ID. |
