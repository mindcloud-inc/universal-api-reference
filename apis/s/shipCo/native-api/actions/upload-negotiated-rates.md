# Upload Negotiated Rates with Ship&Co

## Endpoint

- **Method:** `POST`
- **Path:** `/carriers/:id/rates`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [Upload Negotiated Rates](https://developer.shipandco.com/en/#negotiated-rates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ship&Co carrier ID whose negotiated rates should be uploaded. Ship&Co requires a 17-character carrier ID. Maximum length: 17. |
| `rates[]` | body | `array<object>` | yes | Negotiated rates table array to upload. |
