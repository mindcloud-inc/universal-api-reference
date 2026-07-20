# List fund subfunds with FCA

## Endpoint

- **Method:** `GET`
- **Path:** `/CIS/:prn/Subfund`
- **Base URL:** `https://register.fca.org.uk/services/V0.1`
- **Official documentation:** [List fund subfunds](https://register.fca.org.uk/Developer/s/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prn` | path | `string` | yes | FCA product reference number for a fund or collective investment scheme. |
