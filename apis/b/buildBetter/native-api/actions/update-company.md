# Update Company with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [Update Company](https://docs.buildbetter.ai/pages/CRM%20Integration/companies#company-properties)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | BuildBetter company ID. |
| `name` | body | `string` | no | Updated company name. |
| `domain` | body | `string` | no | Updated company website domain. |
| `color` | body | `string` | no | Updated company color value. |
| `photoUrl` | body | `string` | no | Updated company logo or photo URL. |
