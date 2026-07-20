# Update Client with QDS

## Endpoint

- **Method:** `PUT`
- **Path:** `/clients/:clientId`
- **Base URL:** `https://qdsapp.com/api/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | path | `number` | yes | The QDS client ID. |
| `client.name` | body | `string` | no | Client display name. |
| `client.first_name` | body | `string` | no | Client first name. |
| `client.last_name` | body | `string` | no | Client last name. |
| `client.email` | body | `string` | no | Client email address. |
| `client.reviewer_name` | body | `string` | no | Reviewer display name. |
| `client.city` | body | `string` | no | Client city. |
| `client.branch` | body | `string` | no | Branch or location. |
| `client.mobile` | body | `string` | no | Mobile phone number. |
| `client.contact_number` | body | `string` | no | Contact phone number. |
| `client.survey_frequency` | body | `string` | no | Survey cadence setting. |
| `client.survey_type` | body | `string` | no | Survey type setting. |
| `client.disable_nicejob` | body | `boolean` | no | Whether NiceJob is disabled for the client. |
| `client.status` | body | `string` | no | Client status. |
