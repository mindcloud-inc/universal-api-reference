# Upsert Subscriber Field By Email with Maildroppa

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/fields/by-email`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [Upsert Subscriber Field By Email](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Email address of the subscriber. |
| `fieldTypeId` | body | `string` | no | Unique identifier of the field type. |
| `value` | body | `string` | no | New or updated value for the specified subscriber field. |
