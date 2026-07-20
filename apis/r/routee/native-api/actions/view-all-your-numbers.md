# View all your numbers with Routee

Retrieves all your numbers from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers/my`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [View all your numbers](https://docs.routee.net/reference/view-all-the-numbers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | The page number to retrieve, default value is 0 (meaning the first page) |
| `size` | query | `number` | no | The number of items to retrieve, default value is 20. |
