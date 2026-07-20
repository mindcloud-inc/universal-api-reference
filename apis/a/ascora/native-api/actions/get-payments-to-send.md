# Get Payments To Send with Ascora

Retrieves payments ready to send from Ascora.

## Endpoint

- **Method:** `GET`
- **Path:** `/Accounting/GetPaymentsToSend`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Get Payments To Send](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=76)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `priorToDate` | query | `date` | yes | Only payments dated prior to this date will be included. |
