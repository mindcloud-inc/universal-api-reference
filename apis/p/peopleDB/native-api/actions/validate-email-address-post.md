# Validate Email Address via POST with PeopleDB

Validates an email address in PeopleDB via POST.

## Endpoint

- **Method:** `POST`
- **Path:** `/email_verifications`
- **Base URL:** `https://peopledb.co/api/v1`
- **Official documentation:** [Validate Email Address via POST](https://docs.peopledb.co/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address` | query | `string` | yes | Email address to validate. |
| `smtp_timeout` | query | `number` | no | SMTP check timeout in seconds. |
