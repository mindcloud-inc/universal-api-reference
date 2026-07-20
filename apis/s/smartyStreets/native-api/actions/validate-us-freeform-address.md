# Validate US Freeform Address with Smarty-streets

Retrieves a validated US freeform address from Smarty-streets.

## Endpoint

- **Method:** `GET`
- **Path:** `https://us-street.api.smarty.com/street-address`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Validate US Freeform Address](https://www.smarty.com/docs/apis/us-street-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `street` | query | `string` | yes | Complete address text to verify. |
