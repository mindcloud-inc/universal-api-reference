# Enhance Entity with Diffbot

Enhances a person or organization record in Diffbot.

## Endpoint

- **Method:** `GET`
- **Path:** `https://kg.diffbot.com/kg/v3/enhance`
- **Base URL:** `https://api.diffbot.com`
- **Official documentation:** [Enhance Entity](https://docs.diffbot.com/reference/enhance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Entity name to enhance. |
| `type` | query | `string` | no | Entity type to enhance, such as Person or Organization. |
