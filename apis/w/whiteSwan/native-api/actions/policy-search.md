# Policy Search with White Swan

Retrieves a White Swan policy search by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/policy_search`
- **Base URL:** `https://app.whiteswan.io/api/1.1/wf`
- **Official documentation:** [Policy Search](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/information-calls/policy-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_search` | body | `string` | yes | White Swan policy search ID returned by Submit Complete Plan Request. |
