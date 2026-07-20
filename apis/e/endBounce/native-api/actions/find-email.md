# Find Email with EndBounce

Finds an email in EndBounce by name and domain.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/finder`
- **Base URL:** `https://api.endbounce.com/api/integrations`
- **Official documentation:** [Find Email](https://app.endbounce.com/integrations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Full name to search for. |
| `domain` | body | `string` | yes | Company domain to search against. |
