# Mark Payments Sent with Ascora

Marks payments as sent in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Accounting/MarkPaymentsAsSent`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Mark Payments Sent](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=79)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PaymentIds[]` | body | `string` | yes | Payment IDs to mark as sent. |
