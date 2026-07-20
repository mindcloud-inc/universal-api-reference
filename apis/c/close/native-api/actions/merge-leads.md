# Merge Leads with Close

Merges two leads in Close.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead/merge/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [Merge Leads](https://developer.close.com/resources/leads/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination` | body | `string` | yes | Destination lead ID for merge. |
| `source` | body | `string` | yes | Source lead ID for merge. |
