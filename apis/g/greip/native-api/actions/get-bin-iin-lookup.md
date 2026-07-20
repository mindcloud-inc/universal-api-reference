# Get BIN/IIN Lookup with Greip - Fraud Prevention

Retrieves BIN/IIN lookup data from Greip.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/bin`
- **Base URL:** `https://greipapi.com`
- **Official documentation:** [Get BIN/IIN Lookup](https://docs.greip.io/api-reference/endpoint/data-lookup/bin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bin` | query | `string` | yes | The card BIN or IIN to look up. |
