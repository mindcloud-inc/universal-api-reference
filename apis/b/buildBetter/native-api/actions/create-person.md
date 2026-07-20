# Create Person with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [Create Person](https://docs.buildbetter.ai/pages/CRM%20Integration/people-and-companies#creating-and-editing-profiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Person email address. |
| `firstName` | body | `string` | no | Person first name. |
| `lastName` | body | `string` | no | Person last name. |
| `companyId` | body | `string` | no | Link this person to an existing company ID. |
| `title` | body | `string` | no | Person job title. |
