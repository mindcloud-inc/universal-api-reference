# Create a signal with Middesk

Creates a signal in your Middesk account.

## Endpoint

- **Method:** `POST`
- **Path:** `/signals`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Create a signal](https://docs.middesk.com/reference/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addresses[]` | body | `array` | yes | Addresses associated with the signal. |
| `name` | body | `string` | yes | Business name for the signal. |
