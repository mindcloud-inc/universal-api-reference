# Validate numbers with Bulldog-WP

Validates phone numbers in Bulldog-WP.

## Endpoint

- **Method:** `POST`
- **Path:** `/numbers/validate`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [Validate numbers](https://console.bulldog-wp.co.il/docs/specification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numbers[]` | body | `array<object>` | yes | List of phone numbers to validate and normalize. Send multiple values as a array. |
