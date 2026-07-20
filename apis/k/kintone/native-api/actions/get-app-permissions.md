# Get App Permissions with Kintone

Retrieves app permissions from Kintone.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/acl.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Get App Permissions](https://kintone.dev/en/docs/kintone/rest-api/apps/permissions/get-app-permissions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | query | `number` | yes | The Kintone app ID. |
