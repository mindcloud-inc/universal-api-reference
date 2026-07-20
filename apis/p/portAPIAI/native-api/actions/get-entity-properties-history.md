# Get Entity Properties History with Port API AI

Retrieves entity property history from Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/entities/properties-history`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Get Entity Properties History](https://docs.port.io/api-reference/fetch-the-history-of-an-entitys-properties)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprintIdentifier` | body | `string` | yes | Blueprint identifier. |
| `entityIdentifier` | body | `string` | yes | Entity identifier. |
| `propertyNames[]` | body | `array<string>` | yes | Properties to fetch history for. |
