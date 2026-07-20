# List Tag Definitions with Cerbo

Retrieves tag definitions from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Tag Definitions](https://docs.cer.bo/#tag/Tags/operation/listTags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_deleted` | query | `boolean` | no | Defaults to false, but any non-empty value will include deleted tags in the returned array |
