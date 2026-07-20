# List Segments with MailerLite

Retrieves a page of segments from MailerLite.

## Endpoint

- **Method:** `GET`
- **Path:** `/segments`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [List Segments](https://developers.mailerlite.com/docs/segments#list-all-segments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of segments per page. |
| `page` | query | `number` | no | Page number to fetch, starting from 1. |
