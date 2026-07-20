# Search Contexts with LaunchDarkly

Finds contexts in LaunchDarkly by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectKey/environments/:environmentKey/contexts/search`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Search Contexts](https://launchdarkly.com/docs/api/contexts/search-contexts)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes | The LaunchDarkly environment key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
