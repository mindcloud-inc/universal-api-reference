# Combine Enhancements with Diffbot

Enriches a person and current employer in Diffbot.

## Endpoint

- **Method:** `GET`
- **Path:** `https://kg.diffbot.com/kg/v3/enhance/combine`
- **Base URL:** `https://api.diffbot.com`
- **Official documentation:** [Combine Enhancements](https://docs.diffbot.com/reference/combine)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employer` | query | `string` | no | Current employer name to combine with the person profile. |
| `name` | query | `string` | yes | Person name to combine with employer enrichment. |
