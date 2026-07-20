# Create Datapoint with HoneyHive

Creates a new datapoint in HoneyHive.

## Endpoint

- **Method:** `POST`
- **Path:** `/datapoints`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Create Datapoint](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Project name. |
| `inputs` | body | `object` | yes | Datapoint inputs. |
