# Create Job with AppWright

Creates a new job in AppWright.

## Endpoint

- **Method:** `POST`
- **Path:** `awAPI/awAPI.asp`
- **Base URL:** `https://{clientId}.AppWright.com`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cmd` | query | `string` | yes |
| `ProcessType` | query | `list<string>` | no |
| `JobMode` | query | `list<string>` | no |
| `JobNumber` | query | `string` | no |
| `Order_description` | query | `string` | no |
| `order_resourceid` | query | `string` | no |
| `Order_restypid` | query | `string` | no |
| `Order_ResDesc` | query | `string` | no |
| `Request_Date` | query | `string` | no |
| `udb_lotnumber` | query | `number` | no |
| `udb_address` | query | `string` | no |
| `udb_model` | query | `string` | no |
| `udb_community` | query | `string` | no |
| `udb_customer` | query | `string` | no |
| `udb_abbreviated` | query | `string` | no |
| `udb_elevation` | query | `string` | no |
