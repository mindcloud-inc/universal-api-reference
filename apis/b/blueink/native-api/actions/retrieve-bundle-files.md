# Retrieve Bundle Files with Blueink

Retrieves files for a Blueink bundle.

## Endpoint

- **Method:** `GET`
- **Path:** `/bundles/:bundleSlug/files/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Retrieve Bundle Files](https://developer.blueink.com/api/#tag/Bundles/operation/getBundleFiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bundleSlug` | path | `string` | yes | Bundle slug to retrieve files for. |
