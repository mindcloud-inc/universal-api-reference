# Atomically create a contact group and attach it to an opt-in page with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/opt-in-pages/{pageId}/groups`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Atomically create a contact group and attach it to an opt-in page](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pageId` | path | `string` | yes |
| `title` | body | `string` | yes |
