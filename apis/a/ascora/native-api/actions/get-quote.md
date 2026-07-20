# Get Quote with Ascora

Retrieves a quote from Ascora.

## Endpoint

- **Method:** `GET`
- **Path:** `/Quotes/Quote/{{quoteNumber}}`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Get Quote](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=23)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quoteNumber` | path | `string` | no | Ascora quote number. For sections, use dashes instead of dots, for example Q1234-01. |
