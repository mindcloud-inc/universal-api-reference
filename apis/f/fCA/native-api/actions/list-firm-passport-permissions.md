# List firm passport permissions with FCA

## Endpoint

- **Method:** `GET`
- **Path:** `/Firm/:frn/Passports/:country/Permission`
- **Base URL:** `https://register.fca.org.uk/services/V0.1`
- **Official documentation:** [List firm passport permissions](https://register.fca.org.uk/Developer/s/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `frn` | path | `string` | yes | FCA firm reference number. |
| `country` | path | `string` | yes | Passport country name, for example Gibraltar. |
