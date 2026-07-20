# Delete Subscriber with Mobile Text Alerts

Deletes an existing subscriber from Mobile Text Alerts.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/subscribers/:idOrNumberOrEmail`
- **Base URL:** `https://api.mobile-text-alerts.com/v3`
- **Official documentation:** [Delete Subscriber](https://developers.mobile-text-alerts.com/api-reference/subscribers#delete-subscribers-idornumberoremail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrNumberOrEmail` | path | `string` | yes | Subscriber ID, phone number, or email. |
