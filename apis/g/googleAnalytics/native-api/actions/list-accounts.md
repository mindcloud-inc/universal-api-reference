# List Accounts with Google Analytics

Lists all Google Analytics accounts accessible to the connection.

## Endpoint

- **Method:** `GET`
- **Path:** `https://analyticsadmin.googleapis.com/v1beta/accounts`
- **Base URL:** `https://analyticsdata.googleapis.com/v1beta`
- **Official documentation:** [List Accounts](https://developers.google.com/analytics/devguides/config/admin/v1/rest/v1beta/accounts/list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pageSize` | query | `number` | no |
| `pageToken` | query | `string` | no |
| `showDeleted` | query | `boolean` | no |
