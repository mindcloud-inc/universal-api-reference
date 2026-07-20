# Schedule Agent Launch with PhantomBuster

Schedules an agent launch in PhantomBuster.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/launch-soon`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Schedule Agent Launch](https://hub.phantombuster.com/reference/post_agents-launch-soon)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `argument` | body | `object` | no | — |
| `arguments` | body | `object` | no | — |
| `id` | body | `string` | yes | The PhantomBuster agent ID to schedule for launch. |
| `minutes` | body | `number` | yes | — |
| `saveArgument` | body | `boolean` | no | — |
| `saveArguments` | body | `boolean` | no | — |
