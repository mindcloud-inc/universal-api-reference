# Generate Affiliate Sign-In Link with LeadDyno

Generates a time-limited sign-in link for an affiliate in LeadDyno.

## Endpoint

- **Method:** `POST`
- **Path:** `/affiliates/:id/sign_in_link`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Generate Affiliate Sign-In Link](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/create-a-new-affiliate-copy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The affiliate ID. |
