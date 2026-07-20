# Identify a contact and sync attributes from your app with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/identify`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Identify a contact and sync attributes from your app](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The contact's email address (used as the unique identifier) |
| `firstName` | body | `string` | no | Contact's first name |
| `lastName` | body | `string` | no | Contact's last name |
| `traits` | body | `object` | no | Arbitrary key-value attributes from your app to store on the contact. Keys must be alphanumeric with underscores/hyphens (max 50 chars). Values must be primitives: string, number, or boolean (max 500 chars each). Maximum 10 traits per call. |
