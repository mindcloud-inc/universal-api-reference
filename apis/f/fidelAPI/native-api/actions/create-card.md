# Create Card with Fidel API

Creates a card in a Fidel program.

## Endpoint

- **Method:** `POST`
- **Path:** `/programs/:programId/cards`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Create Card](https://reference.fidel.uk/reference/create-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | path | `string` | yes | — |
| `countryCode` | body | `string` | yes | Allowed values: CAN, DNK, FIN, GBR, IRL, JPN, NOR, SWE, USA. |
| `expMonth` | body | `number` | yes | The value must be between 1 and 12. |
| `expYear` | body | `number` | yes | 4 digits. CurrentYear <= ExpYear <= CurrentYear + 19. |
| `number` | body | `string` | yes | 15-16 long card number. |
| `termsOfUse` | body | `boolean` | yes | Cardholder accepted terms of use. |
