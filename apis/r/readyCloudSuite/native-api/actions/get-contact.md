# Get Contact with ReadyCloud Suite

Retrieves a contact from ReadyCloud Suite.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orgs/:orgPk/contacts/:contactPk/`
- **Base URL:** `https://www.readycloud.com`
- **Official documentation:** [Get Contact](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-12-contacts.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactPk` | path | `string` | yes | ReadyCloud contact identifier. |
| `orgPk` | path | `string` | yes | ReadyCloud organization identifier. |
