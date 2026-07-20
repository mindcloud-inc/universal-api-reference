# List Users with Harness

Retrieves users from Harness.

## Endpoint

- **Method:** `POST`
- **Path:** `/ng/api/user/batch`
- **Base URL:** `https://app.harness.io/gateway`
- **Official documentation:** [List Users](https://apidocs.harness.io/user/getusers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails` | body | `list<string>` | no | Filter by user emails. |
| `identifiers` | body | `list<string>` | no | Filter by user identifiers. |
| `parentFilter` | body | `string` | no | Parent-scope filter mode. |
| `searchTerm` | body | `string` | no | Search users by name or email. |
| `sortOrders` | query | `string` | no | Serialized sort order payload. |
