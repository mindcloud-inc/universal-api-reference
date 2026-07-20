# List Experiments with Omniconvert Explore

Retrieves experiments for a website from Omniconvert Explore.

## Endpoint

- **Method:** `GET`
- **Path:** `/experiments`
- **Base URL:** `https://api.omniconvert.com/v1`
- **Official documentation:** [List Experiments](https://api.omniconvert.com/docs#get--v1-experiments)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Experiment list filter carrier documented by Omniconvert (experiment-type, website-id, experiment-tag). |
