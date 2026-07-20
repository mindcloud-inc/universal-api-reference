# Launch Agent with PhantomBuster

Launches an agent in PhantomBuster.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/launch`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Launch Agent](https://hub.phantombuster.com/reference/post_agents-launch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `argument` | body | `object` | no | — |
| `arguments` | body | `object` | no | — |
| `bonusArgument` | body | `object` | no | — |
| `id` | body | `string` | yes | The PhantomBuster agent ID to launch. |
| `manualLaunch` | body | `boolean` | no | — |
| `maxInstanceCount` | body | `number` | no | — |
| `saveArgument` | body | `boolean` | no | — |
| `saveArguments` | body | `boolean` | no | — |
