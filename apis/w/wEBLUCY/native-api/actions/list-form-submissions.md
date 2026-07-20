# List Form Submissions with WEBLUCY

Retrieves form submissions from WEBLUCY.

## Endpoint

- **Method:** `GET`
- **Path:** `/form-submissions`
- **Base URL:** `https://apps.weblucy.com/api/site`
- **Official documentation:** [List Form Submissions](https://websitebuilder.docs.apiary.io/#reference/form-submissions/list-all-form-submissions/list-all-form-submissions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | List only form submissions created after this Unix timestamp, inclusive. |
| `to` | query | `string` | no | List only form submissions created before this Unix timestamp, inclusive. |
