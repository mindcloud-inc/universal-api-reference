# Update Person with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [Update Person](https://docs.buildbetter.ai/pages/CRM%20Integration/people-and-companies#creating-and-editing-profiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | BuildBetter person ID. |
| `firstName` | body | `string` | no | Updated first name. |
| `lastName` | body | `string` | no | Updated last name. |
| `email` | body | `string` | no | Updated email address. |
| `companyId` | body | `string` | no | Updated linked company ID. |
