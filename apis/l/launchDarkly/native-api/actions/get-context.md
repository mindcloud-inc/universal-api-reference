# Get Context with LaunchDarkly

Retrieves a context from LaunchDarkly by kind and key.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectKey/environments/:environmentKey/contexts/:kind/:key`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Get Context](https://launchdarkly.com/docs/api/contexts/get-contexts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes | The LaunchDarkly environment key. |
| `key` | path | `string` | yes | The LaunchDarkly context key. |
| `kind` | path | `string` | yes | The LaunchDarkly context kind. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
