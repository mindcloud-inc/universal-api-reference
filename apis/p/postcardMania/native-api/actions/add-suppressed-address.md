# Add Suppressed Address with PostcardMania

Creates a new suppressed address in PostcardMania.

## Endpoint

- **Method:** `POST`
- **Path:** `/suppression-list`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Add Suppressed Address](https://docs.pcmintegrations.com/docs/directmail-api/gx39dwmmz7v0z)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Street address to suppress. |
| `city` | body | `string` | yes | City for the suppressed address. |
| `state` | body | `string` | yes | State or province for the suppressed address. |
| `zipCode` | body | `string` | yes | Postal code for the suppressed address. |
