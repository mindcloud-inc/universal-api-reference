# Book Meeting with Hy.page

## Endpoint

- **Method:** `POST`
- **Path:** `/hyax-api/v1/meetings/book`
- **Base URL:** `https://platform.hyax.com`
- **Official documentation:** [Book Meeting](https://platform.hyax.com/api-docs/meetings-book)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notes` | body | `string` | no | Booking notes. |
| `slotId` | body | `string` | yes | Meeting slot ID. |
| `email` | body | `string` | yes | Booker email address. |
| `name` | body | `string` | no | Booker name. |
