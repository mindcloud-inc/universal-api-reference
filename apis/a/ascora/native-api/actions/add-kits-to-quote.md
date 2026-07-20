# Add Kits To Quote with Ascora

Adds kits to a quote in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Quotes/AddKits`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Add Kits To Quote](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=33)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `quoteNumber` | body | `string` | no |
| `quoteKits` | body | `list<object>` | no |
