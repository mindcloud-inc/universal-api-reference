# Update application with Good Grants

Updates an existing application in Good Grants.

## Endpoint

- **Method:** `PUT`
- **Path:** `application/:slug`
- **Base URL:** `https://api.cr4ce.com`
- **Official documentation:** [Update application](https://apidocs.goodgrants.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Application slug |
| `category` | body | `string` | no | Category slug |
| `chapter` | body | `string` | no | Chapter slug |
| `applicant` | body | `string` | no | Applicant slug |
| `title` | body | `string` | no | Application title |
| `status` | body | `string` | no | Application status |
| `moderation_status` | body | `string` | no | Moderation status |
| `grant_end_date` | body | `date` | no | Grant end date |
| `grant_status` | body | `string` | no | Grant status slug |
| `application_fields` | body | `object` | no | Field slug to value map |
| `custom_deadline` | body | `date` | no | Custom deadline |
