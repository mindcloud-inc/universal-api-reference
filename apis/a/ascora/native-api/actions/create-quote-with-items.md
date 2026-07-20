# Create Quote With Items with Ascora

Creates a new quote with items in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Quotes/Quote`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Create Quote With Items](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=37)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `siteCustomer` | body | `object` | no |
| `billingCustomer` | body | `object` | no |
| `quoteName` | body | `string` | no |
| `quoteDescription` | body | `string` | no |
| `quotationDate` | body | `string` | no |
| `pricingMethod` | body | `string` | no |
| `quoteSupplies` | body | `list<object>` | no |
| `quoteKits` | body | `list<object>` | no |
| `quoteLabourItems` | body | `list<object>` | no |
| `quoteWriteIns` | body | `list<object>` | no |
