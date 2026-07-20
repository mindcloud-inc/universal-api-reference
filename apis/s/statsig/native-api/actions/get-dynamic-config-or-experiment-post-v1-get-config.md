# Get Dynamic Config or Experiment with Statsig

Retrieves a dynamic config or experiment from Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/get_config`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Get Dynamic Config or Experiment](https://docs.statsig.com/api-reference/dynamic-configs/get-dynamic-config-or-experiment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configName` | body | `string` | yes | Name of the dynamic config or experiment. |
| `user` | body | `object` | yes | Statsig user object containing at least one identifier. |
| `statsigMetadata` | body | `object` | no | SDK metadata for diagnostics and exposure behavior. |
