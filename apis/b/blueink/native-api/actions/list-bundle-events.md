# List Bundle Events with Blueink

Retrieves event history for a Blueink bundle.

## Endpoint

- **Method:** `GET`
- **Path:** `/bundles/:bundleSlug/events/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [List Bundle Events](https://developer.blueink.com/api/#tag/Bundles/operation/listBundleEvents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bundleSlug` | path | `string` | yes | Bundle slug to inspect events for. |
