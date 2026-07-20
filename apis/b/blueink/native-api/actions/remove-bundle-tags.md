# Remove Bundle Tags with Blueink

Removes tags from a Blueink bundle.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bundles/:bundleSlug/remove_tags/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Remove Bundle Tags](https://developer.blueink.com/api/#tag/Bundles/operation/removeBundleTags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bundleSlug` | path | `string` | yes | Bundle slug to remove tags from. |
| `tags[]` | body | `array<string>` | yes | Tags to remove from the bundle. |
