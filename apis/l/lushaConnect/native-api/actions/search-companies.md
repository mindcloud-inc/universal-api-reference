# Search Companies with Lusha Connect

Finds companies in Lusha Connect by enrichment inputs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/company`
- **Base URL:** `https://api.lusha.com`
- **Official documentation:** [Search Companies](https://docs.lusha.com/apis/openapi/enrichment/searchsinglecompanyv2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companies` | body | `list<object>` | yes | List of company lookup objects. Each item must include id and may include domain, fqdn, name, or companyId. |
