# Validate US Address With Enhanced Matching with Smarty-streets

Retrieves US address validation details from Smarty-streets using enhanced matching.

## Endpoint

- **Method:** `GET`
- **Path:** `https://us-street.api.smarty.com/street-address`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Validate US Address With Enhanced Matching](https://www.smarty.com/docs/apis/us-street-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `street` | query | `string` | yes | Address text to verify with enhanced matching. |
