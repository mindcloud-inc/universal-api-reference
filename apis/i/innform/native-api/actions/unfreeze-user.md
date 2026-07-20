# Unfreeze User with Innform

Unfreezes a user in Innform by ID or email.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/{idOrEmail}/unfreeze`
- **Base URL:** `https://api.innform.io/v1`
- **Official documentation:** [Unfreeze User](https://innform.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrEmail` | path | `string` | yes | User UUID or email address. |
