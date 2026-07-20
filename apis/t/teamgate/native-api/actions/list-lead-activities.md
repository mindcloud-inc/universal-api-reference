# List Lead Activities with Teamgate

Retrieves activities for a lead in Teamgate.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/{{leadId}}/events`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [List Lead Activities](https://developers.teamgate.com/#0b9f8299-f529-45c2-b768-a465b14d4084)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadId` | path | `string` | yes | Lead ID whose activities should be listed. |
