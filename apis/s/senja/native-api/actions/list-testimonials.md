# List Testimonials with Senja

Retrieves testimonials from your Senja project.

## Endpoint

- **Method:** `GET`
- **Path:** `/testimonials`
- **Base URL:** `https://api.senja.io/v1`
- **Official documentation:** [List Testimonials](https://support.senja.io/articles/rest-api-wbnz4#list-testimonials-in-your-senja-project)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `approved` | query | `boolean` | no | Filter testimonials by approval status. |
| `integration` | query | `string` | no | Filter testimonials by integration. |
| `lang` | query | `string` | no | Filter testimonials by language. |
| `rating` | query | `number` | no | Filter testimonials by rating. |
| `tags[]` | query | `array<string>` | no | Filter testimonials by tag. |
| `type` | query | `string` | no | Filter testimonials by type. |
