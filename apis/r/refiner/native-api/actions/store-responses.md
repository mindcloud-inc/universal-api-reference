# Store Responses with Refiner

Stores survey response data in Refiner.

## Endpoint

- **Method:** `POST`
- **Path:** `/responses`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [Store Responses](https://refiner.io/docs/api/#store-responses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Identify the user by your own user ID. |
| `email` | body | `string` | no | Identify the user by email address. |
| `form_uuid` | body | `string` | yes | The Refiner form UUID that will own the stored response. |
| `date` | body | `date` | no | When the survey response was initially recorded. |
| `prevent_duplicates` | body | `boolean` | no | Set to false to disable Refiner's duplicate prevention. |
| `responseData` | body | `object` | no | Key-value pairs where each key matches a Refiner question identifier. |
