# Update Account with Recut URL Shortener

Updates account details in Recut URL Shortener.

## Endpoint

- **Method:** `PUT`
- **Path:** `/account/update`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Update Account](https://app.recut.in/developers#update-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Account email address |
| `password` | body | `string` | no | New account password |
