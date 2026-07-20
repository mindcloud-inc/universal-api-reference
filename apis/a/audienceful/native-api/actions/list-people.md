# List People with Audienceful

Retrieves a list of people from Audienceful.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/`
- **Base URL:** `https://app.audienceful.com/api`
- **Official documentation:** [List People](https://developer.audienceful.com/api-reference/people/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search people that match the provided string. |
| `status` | query | `string` | no | Filter people by status. |
