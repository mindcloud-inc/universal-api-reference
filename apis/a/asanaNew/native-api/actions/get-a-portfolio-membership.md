# Get a portfolio membership with Asana

Retrieves a portfolio membership from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `portfolio_memberships/:portfolio_membership_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a portfolio membership](https://developers.asana.com/reference/getportfoliomembership)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `portfolio_membership_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
