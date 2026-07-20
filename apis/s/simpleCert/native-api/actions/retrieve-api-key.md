# Retrieve API Key with SimpleCert

## Endpoint

- **Method:** `POST`
- **Path:** `/user/api-key`
- **Base URL:** `https://app.simplecert.net/api`
- **Official documentation:** [Retrieve API Key](https://simplecert.readme.io/reference/authentication)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | SimpleCert account login email. |
| `password` | body | `string` | yes | SimpleCert account password. |
