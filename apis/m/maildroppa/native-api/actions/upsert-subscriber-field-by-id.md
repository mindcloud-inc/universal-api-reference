# Upsert Subscriber Field By ID with Maildroppa

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/fields/by-id`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [Upsert Subscriber Field By ID](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldTypeId` | body | `string` | no | Unique identifier of the field type. |
| `subscriberId` | body | `string` | no | Unique identifier of the subscriber. |
| `value` | body | `string` | no | New or updated value for the specified subscriber field. |
