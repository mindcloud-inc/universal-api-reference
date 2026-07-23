# List Flow Proposal For Role with Rillion Prime

## Endpoint

- **Method:** `GET`
- **Path:** `/invoice/FlowProposal/role/:role`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Flow Proposal For Role](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Invoice%20-%20v1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role` | path | `string` | yes | Path value for Role. |
| `headersOnly` | query | `boolean` | no | When true, returns only header rows where supported. |
| `Role` | query | `string` | no | Optional query value for Role. |
| `HeadersOnly` | query | `boolean` | no | When true, returns only header rows where supported. |
