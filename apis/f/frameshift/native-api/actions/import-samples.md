# Import Samples with Frameshift

Imports samples into a Frameshift project.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:project_id/samples/import`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Import Samples](https://mosaic.frameshift.io/api/#api-Samples-ImportSamples)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | — |
| `sample_ids[]` | body | `array<number>` | yes | Send multiple values as a array. |
