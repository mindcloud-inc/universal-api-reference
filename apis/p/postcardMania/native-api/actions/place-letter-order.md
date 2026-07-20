# Place Letter Order with PostcardMania

Creates a new letter order in PostcardMania.

## Endpoint

- **Method:** `POST`
- **Path:** `/order/letter`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Place Letter Order](https://docs.pcmintegrations.com/docs/directmail-api/130adee30e721)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `designID` | body | `string` | no | Existing approved design to use for the letter order. |
| `letter` | body | `string` | no | Raw HTML letter content when not using a design ID. |
| `envelope` | body | `object` | yes | Envelope object required for letter orders. |
| `mailClass` | body | `string` | yes | Mail class for the order. |
| `color` | body | `boolean` | yes | Whether the letter should print in color. |
| `printOnBothSides` | body | `boolean` | yes | Whether to print on both sides. |
| `insertAddressingPage` | body | `boolean` | yes | Whether to insert an addressing page. |
| `recipients[]` | body | `array<object>` | yes | Recipient list for the order. |
