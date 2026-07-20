# Run Company Website Finder with Botster

Creates a Botster company website lookup job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/company-website-finder`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Company Website Finder](https://botster.io/bots/company-website-finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[]` | body | `array<string>` | yes | Links to find, such as About Page or Team/Leadership Page. |
| `input` | body | `string` | yes | Company names. |
