# Create application with Good Grants

Creates a new application in Good Grants.

## Endpoint

- **Method:** `POST`
- **Path:** `application`
- **Base URL:** `https://api.cr4ce.com`
- **Official documentation:** [Create application](https://apidocs.goodgrants.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | yes | Category slug |
| `chapter` | body | `string` | yes | Chapter slug |
| `applicant` | body | `string` | yes | Applicant slug |
| `season` | body | `string` | yes | Season slug |
| `title` | body | `string` | yes | Application title |
| `form` | body | `string` | no | Form slug |
| `status` | body | `string` | no | Application status |
| `moderation_status` | body | `string` | no | Moderation status |
| `grant_end_date` | body | `date` | no | Grant end date |
| `grant_status` | body | `string` | no | Grant status slug |
| `application_fields` | body | `object` | no | Field slug to value map |
| `custom_deadline` | body | `date` | no | Custom deadline |
