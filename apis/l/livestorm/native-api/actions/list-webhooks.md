# List Webhooks with Livestorm

Retrieves webhooks from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `webhooks`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [List Webhooks](https://developers.livestorm.co/reference/get_webhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[event]` | query | `string` | no | Filter Webhooks by event : event.published, event.created, session.started, session.ended, session.created, people.registered, people.attended, people.not_attended, people.watched_replay, job.ended |
