# Create User with Halo Service Solutions

Creates a new user in Halo Service Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/Users`
- **Base URL:** `https://mindcloud.halopsa.com/api`
- **Official documentation:** [Create User](https://usehalo.com/swagger/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `site_id` | body | `number` | yes |
| `firstname` | body | `string` | no |
| `surname` | body | `string` | no |
| `emailaddress` | body | `string` | no |
