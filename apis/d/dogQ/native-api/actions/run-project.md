# Run Project with DogQ

Runs a DogQ project with optional variables and contexts.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/external_execute`
- **Base URL:** `https://dogq.io`
- **Official documentation:** [Run Project](https://docs.dogq.io/documentation/integrations/ci-cd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | Variables to inject into the project execution. |
| `contexts` | body | `object` | no | Datasets for batch project execution. |
