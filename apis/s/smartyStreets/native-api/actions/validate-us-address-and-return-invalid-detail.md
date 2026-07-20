# Validate US Address And Return Invalid Detail with Smarty-streets

Retrieves US address validation details from Smarty-streets, including invalid matches.

## Endpoint

- **Method:** `GET`
- **Path:** `https://us-street.api.smarty.com/street-address`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Validate US Address And Return Invalid Detail](https://www.smarty.com/docs/apis/us-street-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `street` | query | `string` | yes | Address text to verify, including invalid addresses when match is invalid. |
