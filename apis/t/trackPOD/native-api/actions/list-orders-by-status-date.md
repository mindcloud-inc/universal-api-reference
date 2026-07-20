# List Orders By Status Date with Track-POD

Retrieves orders from Track-POD by status date using UTC time.

## Endpoint

- **Method:** `GET`
- **Path:** `/Order/Status/Date/:date`
- **Base URL:** `https://api.track-pod.com`
- **Official documentation:** [List Orders By Status Date](https://api.track-pod.com/index.html#/Order/GetOrderByStatusDate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | UTC date and time used to fetch orders by status change. |
