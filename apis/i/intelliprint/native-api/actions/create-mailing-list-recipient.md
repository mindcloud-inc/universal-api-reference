# Create Mailing List Recipient with Intelliprint

## Endpoint

- **Method:** `POST`
- **Path:** `/mailing_lists/:mailingList/recipients`
- **Base URL:** `https://api.intelliprint.net/v1`
- **Official documentation:** [Create Mailing List Recipient](https://docs.intelliprint.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address.country` | body | `string` | no | ISO 3166-1 alpha-2 country code. |
| `address.line` | body | `string` | yes | The full mailing address line. |
| `address.name` | body | `string` | no | The recipient name printed on the mailing item. |
| `address.postcode` | body | `string` | no | The postal code for the address. |
| `mailing_list` | path | `string` | yes | The Intelliprint mailing list ID. |
| `variables` | body | `object` | no | Dynamic template variables for the recipient. |
