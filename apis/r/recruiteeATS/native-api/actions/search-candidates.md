# Search Candidates with Recruitee ATS

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:company_id/search/new/candidates`
- **Base URL:** `https://api.recruitee.com`
- **Official documentation:** [Search Candidates](https://docs.recruitee.com/reference/searchnewcandidates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters_json` | query | `string` | no | Array of filters serialized to a JSON string, as documented by Recruitee. |
| `sort_by` | query | `string` | no | Sort order with _asc or _desc suffix, for example created_at_desc. |
