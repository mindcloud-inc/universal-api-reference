# List Poll Receipts with Loomio

Retrieves poll receipts from Loomio.

## Endpoint

- **Method:** `GET`
- **Path:** `/polls/:id/receipts`
- **Base URL:** `https://www.loomio.com/api/v1`
- **Official documentation:** [List Poll Receipts](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/polls_controller.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | The Loomio poll ID. |
