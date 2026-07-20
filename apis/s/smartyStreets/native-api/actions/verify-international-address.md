# Verify International Address with Smarty-streets

Retrieves international address verification details from Smarty-streets.

## Endpoint

- **Method:** `GET`
- **Path:** `https://international-street.api.smarty.com/verify`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Verify International Address](https://www.smarty.com/docs/apis/international-street-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Country name or ISO country code. |
| `freeform` | query | `string` | yes | Entire address minus the country. |
