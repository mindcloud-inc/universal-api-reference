# Get Subscriber with Mobile Text Alerts

Finds a subscriber in Mobile Text Alerts by ID, number, or email.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/:idOrNumberOrEmail`
- **Base URL:** `https://api.mobile-text-alerts.com/v3`
- **Official documentation:** [Get Subscriber](https://developers.mobile-text-alerts.com/api-reference/subscribers#get-subscribers-idornumberoremail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrNumberOrEmail` | path | `string` | yes | Subscriber ID, phone number, or email. |
