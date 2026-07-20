# View all the available numbers with Routee

Retrieves all the available numbers from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers/available`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [View all the available numbers](https://docs.routee.net/reference/view-all-the-available-numbers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | The country of the recipient in ISO 3166-1 alpha 2 format. |
| `service` | query | `string` | no | The available services are "Sms" and "Voice" (case sensitive) |
| `page` | query | `number` | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | query | `number` | no | The number of items to retrieve, default value is 20. |
| `sort` | query | `string` | no | The field name that will be used to sort the results. |
| `areaCode` | query | `number` | no | Area code is a 3-digit prefix applied only for US numbers(1-xxx-123456). |
