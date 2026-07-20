# Verify Recipient with Recommand

Verifies a recipient in the Recommand directory.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/verify`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Verify Recipient](https://recommand.eu/en/reference/recipients/verify-recipient)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeBusinessCard` | body | `boolean` | no | If true, fetches the business card from the SMP for company name and country. |
| `includeEndpointDetails` | body | `boolean` | no | If true, fetches endpoint details for all supported document types. |
| `peppolAddress` | body | `string` | yes | The Peppol address of the recipient to verify. |
