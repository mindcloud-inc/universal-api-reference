# List Contacts with Zoho Campaigns

Retrieves contacts from a Zoho Campaigns list.

## Endpoint

- **Method:** `GET`
- **Path:** `/getlistsubscribers`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [List Contacts](https://www.zoho.com/campaigns/help/developers/get-list-subscribers.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listkey` | query | `list<string>` | yes | Mailing list key to read contacts from. |
| `sort` | query | `list<string>` | no | Sort direction for the returned contacts. Accepted values: `asc`, `desc`. |
| `status` | query | `list<string>` | no | Contact status bucket to include in the results. Accepted values: `active`, `bounce`, `mostrecent`, `recent`, `unsub`. |
