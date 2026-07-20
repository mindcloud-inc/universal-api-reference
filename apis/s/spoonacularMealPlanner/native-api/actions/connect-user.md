# Connect User with Spoonacular Meal Planner

Creates a connected user in Spoonacular Meal Planner.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/connect`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Connect User](https://spoonacular.com/food-api/docs#Connect-User)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | User's email address. |
| `firstName` | body | `string` | no | User's first name. |
| `lastName` | body | `string` | no | User's last name. |
| `username` | body | `string` | no | Your app user's username for Spoonacular connection. |
