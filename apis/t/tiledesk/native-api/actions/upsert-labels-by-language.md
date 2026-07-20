# Upsert Labels By Language with Tiledesk

Upserts labels for a language in Tiledesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/{projectId}/labels/:lang`
- **Base URL:** `https://api.tiledesk.com/v3`
- **Official documentation:** [Upsert Labels By Language](https://developer.tiledesk.com/apis/rest-api/labels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lang` | path | `string` | yes | The label language code. |
