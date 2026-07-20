# Update Quote Status with Ascora

Updates the status of a quote in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Quotes/UpdateStatus`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Update Quote Status](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=44)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quoteNumber` | body | `string` | no | — |
| `quoteStatus` | body | `string` | no | IN-PROGRESS, SENT-TO-CUSTOMER, LOST, or WON. |
| `reasonForLoss` | body | `string` | no | Applied when the quote status is LOST. |
