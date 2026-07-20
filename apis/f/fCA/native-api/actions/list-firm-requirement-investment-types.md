# List firm requirement investment types with FCA

## Endpoint

- **Method:** `GET`
- **Path:** `/Firm/:frn/Requirements/:reqRef/InvestmentTypes`
- **Base URL:** `https://register.fca.org.uk/services/V0.1`
- **Official documentation:** [List firm requirement investment types](https://register.fca.org.uk/Developer/s/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `frn` | path | `string` | yes | FCA firm reference number. |
| `reqRef` | path | `string` | yes | FCA requirement reference number. |
