# Proposal Search with Sunwise

Finds proposals in Sunwise by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/proposals/proposal-search/`
- **Base URL:** `https://production.sunwise.ai/boty/api/v1`
- **Official documentation:** [Proposal Search](https://production.sunwise.ai/boty/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search term for matching proposals |
