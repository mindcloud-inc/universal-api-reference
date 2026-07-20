# Add Study User with Castor EDC

Adds a user to a study in Castor EDC.

## Endpoint

- **Method:** `POST`
- **Path:** `/study/:study_id/user`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Add Study User](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `email` | body | `string` | yes | Email address of the user to invite |
| `send_invite_email` | body | `boolean` | no | Whether to send the invitation email |
| `message` | body | `string` | no | Optional invitation message |
| `default_role_assignment` | body | `number` | no | Default study role assignment ID |
