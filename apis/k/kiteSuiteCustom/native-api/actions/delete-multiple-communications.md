# Delete multiple communications. with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/communication/multiple-delete`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Delete multiple communications.](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `communicationIds[]` | body | `array` | yes | List of communication IDs to be deleted. |
| `isDeleteThread` | body | `boolean` | yes | Flag to indicate if the entire thread should be deleted. |
