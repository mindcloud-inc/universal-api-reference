# Update Bundle with Blueink

Updates an existing bundle in Blueink.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/bundles/:bundleSlug/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Update Bundle](https://developer.blueink.com/api/#tag/Bundles/operation/updateBundlePartial)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bundleSlug` | path | `string` | yes | Bundle slug to update. |
| `cc_sender` | body | `boolean` | no | Whether to cc the sender when the bundle completes. |
