# List Properties with Google Analytics

## Endpoint

- **Method:** `GET`
- **Path:** `https://analyticsadmin.googleapis.com/v1beta/properties`
- **Base URL:** `https://analyticsdata.googleapis.com/v1beta`
- **Official documentation:** [List Properties](https://developers.google.com/analytics/devguides/config/admin/v1/rest/v1beta/properties/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | yes | Required Admin API filter, for example parent:accounts/123456789 |
| `pageSize` | query | `number` | no | — |
| `pageToken` | query | `string` | no | — |
| `showDeleted` | query | `boolean` | no | — |
