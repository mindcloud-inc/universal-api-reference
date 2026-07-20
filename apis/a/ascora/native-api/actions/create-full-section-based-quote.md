# Create Full Section-Based Quote with Ascora

Creates a new section-based quote in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Quotes/Quote`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Create Full Section-Based Quote](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=41)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `siteCustomer` | body | `object` | no |
| `pricingMethod` | body | `string` | no |
| `childQuotes` | body | `list<object>` | no |
| `quoteName` | body | `string` | no |
| `quoteDescription` | body | `string` | no |
