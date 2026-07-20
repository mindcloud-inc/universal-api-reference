# Add Quote Sections with Ascora

Adds sections to a quote in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Quotes/AddQuoteSections`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Add Quote Sections](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=40)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quoteNumber` | body | `string` | no | Full Ascora quote number. Use the full quote number for a section, for example Q1234.01. |
| `quoteSections` | body | `list<object>` | no | Array of section objects with name and displayOrder. |
