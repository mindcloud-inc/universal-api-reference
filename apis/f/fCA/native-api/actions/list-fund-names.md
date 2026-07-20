# List fund names with FCA

## Endpoint

- **Method:** `GET`
- **Path:** `/CIS/:prn/Names`
- **Base URL:** `https://register.fca.org.uk/services/V0.1`
- **Official documentation:** [List fund names](https://register.fca.org.uk/Developer/s/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prn` | path | `string` | yes | FCA product reference number for a fund or collective investment scheme. |
