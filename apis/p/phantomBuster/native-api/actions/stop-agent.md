# Stop Agent with PhantomBuster

Stops a running agent in PhantomBuster.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/stop`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Stop Agent](https://hub.phantombuster.com/reference/post_agents-stop)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cascadeToAllSlaves` | body | `boolean` | no | — |
| `dontLaunchSoon` | body | `boolean` | no | — |
| `id` | body | `string` | yes | The PhantomBuster agent ID to stop. |
| `softAbort` | body | `boolean` | no | — |
| `switchToManualLaunch` | body | `boolean` | no | — |
