# Save Variant with Wafrow

Creates a saved personalization variant in Wafrow.

## Endpoint

- **Method:** `POST`
- **Path:** `/storeVariant/:templateID`
- **Base URL:** `https://wafrow.com/api`
- **Official documentation:** [Save Variant](https://wafrow.com/docs/api#/operations/variant.store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateID` | path | `string` | yes | The Wafrow template UUID to save a personalization preset for. |
| `personalize` | body | `object` | no | Layer overrides keyed by template layer name. |
