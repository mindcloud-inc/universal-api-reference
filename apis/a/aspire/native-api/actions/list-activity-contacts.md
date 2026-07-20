# List Activity Contacts with Aspire

Retrieves activity contacts from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `ActivityContacts`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Activity Contacts](https://cloud-api.youraspire.com/swagger/index.html#/ActivityContacts/ActivityContacts_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
