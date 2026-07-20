# Publish Translations with SimpleLocalize

Publishes translations to an environment in SimpleLocalize.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/environments/{environmentKey}/publish`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Publish Translations](https://api.simplelocalize.io/openapi/ui#/Hosting/publishTranslations)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes |
| `labels[]` | body | `array<string>` | no |
