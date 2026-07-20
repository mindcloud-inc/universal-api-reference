# Create Subscriber with Kit

Creates a new subscriber in Kit.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [Create Subscriber](https://developers.kit.com/api-reference/subscribers/create-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address` | body | `string` | yes | Email address for the subscriber to create. |
| `state` | body | `list<string>` | no | Initial subscriber state. Accepted values: `active`, `bounced`, `cancelled`, `complained`, `inactive`. |
