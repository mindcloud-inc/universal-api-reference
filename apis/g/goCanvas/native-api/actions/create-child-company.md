# Create Child Company with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/companies`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Create Child Company](https://api.gocanvas.com/api/v3/docs#create-a-child-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name` | body | `string` | yes | Name of the new child company. |
| `email` | body | `string` | yes | Email and login for the new company's administrator. |
| `first_name` | body | `string` | yes | First name of the new company's administrator. |
| `last_name` | body | `string` | yes | Last name of the new company's administrator. |
| `seat_count` | body | `number` | no | Licensed seat count; 0 means unlimited. GoCanvas defaults to 1. |
| `password` | body | `string` | no | Initial password for the administrator. |
| `phone` | body | `string` | no | Phone number of the administrator. |
| `country` | body | `string` | no | Administrator's country; also determines the company's date format. |
| `base_url` | body | `string` | no | Child account's Simpro URL; required for Simpro partnerships. |
| `pendo_account_id` | body | `string` | no | Analytics correlation identifier; applies only to Simpro partnerships. |
