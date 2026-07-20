# Create Recognition Request with Tiliter

Creates a recognition request in the Tiliter Recognition API.

## Endpoint

- **Method:** `POST`
- **Path:** `/recognition/`
- **Base URL:** `https://recognition.services.tiliter.com/v1/15`
- **Official documentation:** [Create Recognition Request](https://developer.tiliter.com/docs/overview-of-the-operational-endpoints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `deviceId` | body | `string` | yes |
| `images[]` | body | `array<object>` | yes |
| `weightGrams` | body | `number` | no |
| `includeScores` | body | `boolean` | no |
| `maxOptions` | body | `number` | no |
