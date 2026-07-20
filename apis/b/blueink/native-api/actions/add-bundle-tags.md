# Add Bundle Tags with Blueink

Adds tags to a Blueink bundle.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bundles/:bundleSlug/add_tags/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Add Bundle Tags](https://developer.blueink.com/api/#tag/Bundles/operation/addBundleTags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bundleSlug` | path | `string` | yes | Bundle slug to add tags to. |
| `tags[]` | body | `array<string>` | yes | Tags to add to the bundle. |
