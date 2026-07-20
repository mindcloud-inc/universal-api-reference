# Create Lead Finder Search with BetterContact

Creates an asynchronous BetterContact lead finder search.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead_finder/async`
- **Base URL:** `https://app.bettercontact.rocks/api/v2`
- **Official documentation:** [Create Lead Finder Search](https://doc.bettercontact.rocks/api-reference/endpoint/lead_finder_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | Lead finder filters object, for example {"company":{"include":["OpenAI"]},"lead_seniority":{"include":["founder"]}}. |
| `max_leads` | body | `number` | yes | Maximum number of leads to return. |
