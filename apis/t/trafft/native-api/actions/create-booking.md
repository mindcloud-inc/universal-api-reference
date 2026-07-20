# Create Booking with Trafft

Creates a new booking in Trafft.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings`
- **Base URL:** `https://mindcloud.admin.trafft.com/api/v2`
- **Official documentation:** [Create Booking](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service` | body | `number` | yes | Trafft service ID. |
| `employee` | body | `number` | yes | Trafft employee ID. |
| `date` | body | `string` | yes | Booking date in YYYY-MM-DD format. |
| `time` | body | `string` | yes | Booking start time in HH:mm format. |
| `customer` | body | `number` | yes | Trafft customer ID. |
