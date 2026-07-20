# Clear Quote Items with Ascora

Clears items from a quote in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Quotes/ClearQuoteItems`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Clear Quote Items](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=39)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `quoteNumber` | body | `string` | no |
| `removeSupplies` | body | `boolean` | no |
| `removeKits` | body | `boolean` | no |
| `removeLabour` | body | `boolean` | no |
