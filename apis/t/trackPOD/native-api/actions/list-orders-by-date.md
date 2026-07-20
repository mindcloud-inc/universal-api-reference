# List Orders By Date with Track-POD

Retrieves orders from Track-POD by date.

## Endpoint

- **Method:** `GET`
- **Path:** `/Order/Date/:date`
- **Base URL:** `https://api.track-pod.com`
- **Official documentation:** [List Orders By Date](https://api.track-pod.com/index.html#/Order/GetOrderByDate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | Date and time used to fetch orders. |
