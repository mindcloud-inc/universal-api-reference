# Upsert Admin with Classe365

Creates or updates an admin in Classe365.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/admin`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Upsert Admin](https://speca.io/classe365/academics#insert-update-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | body | `string` | no | Admin contact number. |
| `email_address` | body | `string` | no | Admin email. |
| `id` | body | `string` | no | Admin id for updates. |
| `name` | body | `string` | no | Admin name. |
