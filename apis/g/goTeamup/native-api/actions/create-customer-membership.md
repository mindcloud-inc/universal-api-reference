# Create Customer Membership with GoTeamup

Creates a new customer membership in GoTeamup.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer_memberships`
- **Base URL:** `https://goteamup.com/api/v2`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | body | `number` | yes | Customer ID |
| `membership` | body | `number` | yes | Membership ID |
