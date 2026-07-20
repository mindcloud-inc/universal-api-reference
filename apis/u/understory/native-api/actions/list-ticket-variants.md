# List Ticket Variants with Understory

Retrieves ticket variants for an experience in Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/experiences/{{experienceId}}/ticket-variants`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [List Ticket Variants](https://developer.understory.io/apis/experience/getticketvariantsforexperience.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept-Language` | `en-GB` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experienceId` | path | `string` | yes | The unique identifier of the experience. |
