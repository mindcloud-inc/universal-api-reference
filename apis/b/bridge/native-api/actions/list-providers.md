# List Providers with Bridge

Retrieves supported providers from Bridge.

## Endpoint

- **Method:** `GET`
- **Path:** `/providers`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [List Providers](https://docs.bridgeapi.io/reference/getproviders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Filter the countries you need. When multiple values are specified, they are combined using an `OR` operation |
| `capabilities` | query | `string` | no | Filter the provider capabilities you need. When multiple values are specified, they are combined using an `AND` operation |
| `aggregation_release_status` | query | `string` | no | Filter the deployment states of the providers' aggregation capabilities. When multiple values are specified, they are combined using an `OR` operation |
| `payment_release_status` | query | `string` | no | Filter the deployment states of the providers' payment capabilities. When multiple values are specified, they are combined using an `OR` operation |
| `segment` | query | `string` | no | Filter the segment of the providers. When multiple values are specified, they are combined using an `OR` operation |
| `provider_environments` | query | `string` | no | Filter the environment of the providers. When multiple values are specified, they are combined using an `OR` operation |
