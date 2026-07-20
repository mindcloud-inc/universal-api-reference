# Upsert Environment Variable with Particle

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/env/:key`
- **Base URL:** `https://api.particle.io`
- **Official documentation:** [Upsert Environment Variable](https://docs.particle.io/reference/cloud-apis/api/#set-environment-variable)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `key` | path | `string` | yes |
| `value` | body | `string` | yes |
