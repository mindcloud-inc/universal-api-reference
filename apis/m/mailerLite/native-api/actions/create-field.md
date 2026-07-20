# Create Field with MailerLite

Creates a subscriber field in MailerLite.

## Endpoint

- **Method:** `POST`
- **Path:** `/fields`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Create Field](https://developers.mailerlite.com/docs/fields#create-a-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Field name. |
| `type` | body | `string` | yes | Field type. |
