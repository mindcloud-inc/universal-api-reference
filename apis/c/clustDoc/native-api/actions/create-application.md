# Create Application with ClustDoc

## Endpoint

- **Method:** `POST`
- **Path:** `/dossiers`
- **Base URL:** `https://api.clustdoc.com/api`
- **Official documentation:** [Create Application](https://clustdoc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact.email` | body | `string` | yes | Primary contact email for the application. |
| `contact.firstname` | body | `string` | yes | Primary contact first name. |
| `contact.lastname` | body | `string` | yes | Primary contact last name. |
| `template_id` | body | `string` | yes | The template ID used to create the application. |
