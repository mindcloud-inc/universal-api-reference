# List Branches with Aspire

Retrieve a list of information related to branches in an organization.

## Endpoint

- **Method:** `GET`
- **Path:** `Branches`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Branches](https://guide.youraspire.com/apidocs/branches-7)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
