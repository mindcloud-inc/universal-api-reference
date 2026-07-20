# Identify User with Refiner

Creates or updates a user in Refiner.

## Endpoint

- **Method:** `POST`
- **Path:** `/identify-user`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [Identify User](https://refiner.io/docs/api/#identify-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Identify the user by your own user ID. |
| `email` | body | `string` | no | Identify the user by email address. |
| `attributes` | body | `object` | no | Additional contact traits to merge into the Refiner contact. |
| `account` | body | `object` | no | Optional account object to group multiple contacts under one account. |
