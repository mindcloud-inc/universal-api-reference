# Cancel Book Transfer with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/transfers/book/:book_transfer_id/cancel`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Cancel Book Transfer](https://column.com/docs/api/#book-transfer/cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `book_transfer_id` | path | `string` | yes | ID of the book transfer hold to cancel. |
