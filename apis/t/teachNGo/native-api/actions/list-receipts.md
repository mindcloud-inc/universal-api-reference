# List Receipts with Teach 'n Go

Retrieves receipts from Teach 'n Go.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/receipts`
- **Base URL:** `https://app.teachngo.com`
- **Official documentation:** [List Receipts](https://intercom.help/teach-n-go/en/articles/8727904-teach-n-go-api-endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_date` | body | `date` | no | Only return receipts issued on or after this date. |
| `to_date` | body | `date` | no | Only return receipts issued on or before this date. |
