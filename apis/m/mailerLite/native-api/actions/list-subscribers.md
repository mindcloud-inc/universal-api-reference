# List Subscribers with MailerLite

Retrieves a page of subscribers from MailerLite.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [List Subscribers](https://developers.mailerlite.com/docs/subscribers#list-all-subscribers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of subscribers per page (up to 100). |
| `page` | query | `number` | no | Page number to fetch. |
