# Create Company with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [Create Company](https://docs.buildbetter.ai/pages/CRM%20Integration/people-and-companies#creating-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Company name. |
| `domain` | body | `string` | no | Company website domain. |
| `color` | body | `string` | no | Company color value. |
| `photoUrl` | body | `string` | no | Company logo or photo URL. |
