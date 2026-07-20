# Initiate Password Reset with Outseta

Initiates a password reset for a person in Outseta.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/people/forgotPassword`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Initiate Password Reset](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `parentUrl` | query | `string` | yes |
| `Email` | body | `string` | no |
