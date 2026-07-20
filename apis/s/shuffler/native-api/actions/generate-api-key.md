# Generate API Key with Shuffler

Creates an API key in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/generateapikey`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Generate API Key](https://shuffler.io/docs/API#get-new-apikey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | body | `string` | yes | Target user identifier. |
