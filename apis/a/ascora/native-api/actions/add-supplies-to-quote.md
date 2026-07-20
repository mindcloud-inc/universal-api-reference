# Add Supplies To Quote with Ascora

Adds supplies to a quote in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Quotes/AddSupplies`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Add Supplies To Quote](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=32)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `quoteNumber` | body | `string` | no |
| `quoteSupplies` | body | `list<object>` | no |
