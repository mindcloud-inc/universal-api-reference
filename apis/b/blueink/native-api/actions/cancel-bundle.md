# Cancel Bundle with Blueink

Cancels an existing bundle in Blueink.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bundles/:bundleSlug/cancel/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Cancel Bundle](https://developer.blueink.com/api/#tag/Bundles/operation/cancelBundle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bundleSlug` | path | `string` | yes | Bundle slug to cancel. |
