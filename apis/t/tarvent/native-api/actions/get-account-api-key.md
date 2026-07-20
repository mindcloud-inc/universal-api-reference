# Get Account API Key with Tarvent

Retrieves an account API key from Tarvent by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.tarvent.com`
- **Official documentation:** [Get Account API Key](https://developer.tarvent.com/queries/accountApiKey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | The Tarvent account API key ID to fetch. |
