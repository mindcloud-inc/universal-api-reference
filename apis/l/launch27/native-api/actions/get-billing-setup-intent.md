# Get Billing Setup Intent with Launch27

Retrieves a billing setup intent from Launch27.

## Endpoint

- **Method:** `POST`
- **Path:** `setup/billing/setup_intent`
- **Base URL:** `https://{subdomain}.launch27.com/v1`
- **Official documentation:** [Get Billing Setup Intent](https://api.launch27.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Customer email used to request a billing setup intent. |
