# Login vendor with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/login`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Login vendor](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `login` | body | `string` | yes | Vendor login |
| `password` | body | `string` | yes | Password (should contain at least 1 number, 1 capital and 1 lowercase letter and be 8 more characters long) |
