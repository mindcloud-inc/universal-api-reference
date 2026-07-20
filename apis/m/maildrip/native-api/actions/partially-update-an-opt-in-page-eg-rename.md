# Partially update an opt-in page (e.g. rename) with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/opt-in-pages/{pageId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Partially update an opt-in page (e.g. rename)](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | — |
| `title` | body | `string` | no | New title for the opt-in page |
