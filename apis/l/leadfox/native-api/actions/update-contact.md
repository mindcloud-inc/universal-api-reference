# Update Contact with Leadfox

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/save/`
- **Base URL:** `https://app.leadfox.co/service`
- **Official documentation:** [Update Contact](https://cdn.leadfox.co/upload/7/api_leadfox_12_12-2017.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Contact email address (mandatory). |
| `lifecycle` | body | `string` | yes | Contact lifecycle stage. Allowed values: subscriber, lead, mql, sql, customer. |
| `firstname` | body | `string` | no | Contact first name. |
| `lastname` | body | `string` | no | Contact last name. |
