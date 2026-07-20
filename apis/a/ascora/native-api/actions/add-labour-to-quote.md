# Add Labour To Quote with Ascora

Adds labour items to a quote in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Quotes/AddLabourItems`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Add Labour To Quote](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=36)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `quoteNumber` | body | `string` | no |
| `quoteLabourItems` | body | `list<object>` | no |
