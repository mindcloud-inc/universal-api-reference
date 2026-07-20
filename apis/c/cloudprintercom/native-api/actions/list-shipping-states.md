# List Shipping States with Cloudprinter.com

Retrieves shipping states from Cloudprinter.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/cloudcore/1.0/shipping/states`
- **Base URL:** `https://api.cloudprinter.com`
- **Official documentation:** [List Shipping States](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#list-shipping-states)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_reference` | body | `string` | yes | Country code in ISO 3166-1 alpha-2 format. |
