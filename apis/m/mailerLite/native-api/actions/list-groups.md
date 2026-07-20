# List Groups with MailerLite

Retrieves a page of groups from MailerLite.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [List Groups](https://developers.mailerlite.com/docs/groups#list-all-groups)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of groups per page. |
| `page` | query | `number` | no | Page number to fetch, starting from 1. |
| `filter[name]` | query | `string` | no | Return groups whose names partially match this value. |
| `sort` | query | `string` | no | Sort groups by a supported field, optionally prefixed with - for descending order. |
