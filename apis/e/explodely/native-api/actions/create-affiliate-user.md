# Create Affiliate User with Explodely

Creates a new affiliate user in Explodely.

## Endpoint

- **Method:** `POST`
- **Path:** `/aff`
- **Base URL:** `https://explodely.com/api/v1`
- **Official documentation:** [Create Affiliate User](https://docs.explodely.com/api/create-affiliate-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affusername` | body | `string` | yes | The username for the affiliate account you want to create. |
| `userpass` | body | `string` | yes | The password for the new affiliate account. |
| `fname` | body | `string` | yes | The affiliate user's first name. |
| `lname` | body | `string` | yes | The affiliate user's last name. |
| `email` | body | `string` | yes | The affiliate user's email address. |
| `ipadd` | body | `string` | yes | The affiliate user's IP address. |
