# Print Delivery Labels with Shippify

Retrieves PDF delivery labels from Shippify.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/integrations/deliveries/labels`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deliveryIds[]` | body | `array<string>` | yes | Required array of Shippify delivery identifiers whose labels should be generated. |
| `referenceIds[]` | body | `array<string>` | no | Optional array of Shippify delivery reference identifiers whose labels should be generated. |
