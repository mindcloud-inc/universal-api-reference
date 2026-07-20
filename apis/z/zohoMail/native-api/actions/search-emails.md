# Search Emails with Zoho Mail

Finds emails in Zoho Mail by search parameters.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/messages/search`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Search Emails](https://www.zoho.com/mail/help/api/get-search-emails.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `searchKey` | query | `string` | yes | Search criteria string in Zoho Mail search syntax, for example from:welcome@zoho.com or has:attachment. |
| `receivedTime` | query | `number` | no | Limit search to emails received within the given number of days. |
| `includeto` | query | `boolean` | no | Whether recipient fields should be included in the search scope. |
