# Validate US Street Address with Smarty-streets

Retrieves validated US street addresses from Smarty-streets.

## Endpoint

- **Method:** `GET`
- **Path:** `/street-address`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Validate US Street Address](https://www.smarty.com/docs/apis/us-street-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `street` | query | `string` | yes | Street line of the address. |
| `city` | query | `string` | yes | City name for the address. |
| `state` | query | `string` | yes | State name or abbreviation. |
