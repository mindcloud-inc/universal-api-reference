# Delete Labels By Language with Tiledesk

Deletes labels for a language from Tiledesk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/{projectId}/labels/:lang`
- **Base URL:** `https://api.tiledesk.com/v3`
- **Official documentation:** [Delete Labels By Language](https://developer.tiledesk.com/apis/rest-api/labels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lang` | path | `string` | yes | The label language code. |
