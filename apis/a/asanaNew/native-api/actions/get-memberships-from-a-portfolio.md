# Get memberships from a portfolio with Asana

Retrieves portfolio memberships from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `portfolios/:portfolio_gid/portfolio_memberships`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get memberships from a portfolio](https://developers.asana.com/reference/getportfoliomembershipsforportfolio)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portfolio_gid` | path | `string` | yes | Asana portfolio gid parameter. |
| `user` | query | `string` | no | Asana user parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `limit` | query | `number` | no | Asana limit parameter. |
| `offset` | query | `string` | no | Asana offset parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
