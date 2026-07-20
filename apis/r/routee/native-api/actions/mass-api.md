# Mass API with Routee

Creates a mass data request in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/data`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Mass API](https://docs.routee.net/reference/mass-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Array of objects with data from DB |
| `uuid` | body | `string` | yes | authorization UUID ( Generated from WayMore authorization endpoint and will be provided after contact with the Tech Department) |
| `name` | body | `string` | yes | Name of the data sent e.g.  Customers, Subscribers etc |
| `description` | body | `string` | yes | A short description of the data sent |
| `object[]` | body | `array<object>` | yes | Array of objects and each object contains the data of the same type e.g. customers |
