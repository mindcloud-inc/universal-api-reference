# List Bookings with BoothBook

Retrieves bookings from BoothBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/get/bookings`
- **Base URL:** `https://mindcloud.boothbook.com`
- **Official documentation:** [List Bookings](https://v1-support.boothbook.com/article/endpoint-bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | body | `date` | no | Start date in ISO format (YYYY-MM-DD). |
| `end` | body | `date` | no | End date in ISO format (YYYY-MM-DD). |
| `scope` | body | `string` | no | Use minimal or full to control booking response detail. |
