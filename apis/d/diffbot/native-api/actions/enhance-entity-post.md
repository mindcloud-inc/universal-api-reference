# Enhance Entity (POST) with Diffbot

Enhances a person or organization record in Diffbot using POST.

## Endpoint

- **Method:** `POST`
- **Path:** `https://kg.diffbot.com/kg/v3/enhance`
- **Base URL:** `https://api.diffbot.com`
- **Official documentation:** [Enhance Entity (POST)](https://docs.diffbot.com/reference/enhance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Entity name to enhance. |
| `type` | body | `string` | no | Entity type to enhance, such as Person or Organization. |
