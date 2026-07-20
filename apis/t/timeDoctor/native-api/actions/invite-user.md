# Invite User with Time Doctor

Creates a new user invitation in Time Doctor.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.1/invitations`
- **Base URL:** `https://api2.timedoctor.com`
- **Official documentation:** [Invite User](https://api2.timedoctor.com/#operation/postInvitation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email of the invited user. |
| `name` | body | `string` | no | Optional full name of the invited user. |
| `role` | body | `string` | no | Role of the invited user in the company. |
