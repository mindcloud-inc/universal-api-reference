# Merge Contacts with respond.io

Merges two contacts in respond.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/merge`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [Merge Contacts](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1merge/post?fromExportButton=true&snapshotType=http_operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactIds` | body | `object` | yes | IDs of the two contacts to merge. |
