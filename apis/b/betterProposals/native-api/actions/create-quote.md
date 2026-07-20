# Create Quote with Better Proposals

Creates a quote in Better Proposals.

## Endpoint

- **Method:** `POST`
- **Path:** `/quote/create`
- **Base URL:** `https://api.betterproposals.io`
- **Official documentation:** [Create Quote](https://betterproposals.io/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CompanyID` | body | `string` | yes | Company ID. |
| `TemplateID` | body | `string` | no | Template ID. If provided, Better Proposals retrieves the amount from the template. |
