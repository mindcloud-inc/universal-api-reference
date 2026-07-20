# List Speakers with Sessionize

Retrieves event speaker profiles from Sessionize.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:endpointId/view/Speakers`
- **Base URL:** `https://sessionize.com`
- **Official documentation:** [List Speakers](https://sessionize.com/playbook/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpointId` | path | `string` | yes | Sessionize event API endpoint ID from URLs like https://sessionize.com/api/v2/{endpointId}/view/Speakers. |
