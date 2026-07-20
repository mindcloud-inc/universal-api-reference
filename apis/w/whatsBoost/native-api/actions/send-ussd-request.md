# Send USSD Request with WhatsBoost

Sends a USSD request from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/send/ussd`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Send USSD Request](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | MMI request code. Please make sure that you are using a valid MMI code, if not, it will fail. |
| `sim` | body | `number` | yes | SIM slot number you want to use. |
| `device` | body | `string` | yes | Linked device unique ID. You can get linked device unique ID from /get/devices (Your devices). |
