# List Payment Images with Rillion Prime Pay

## Endpoint

- **Method:** `GET`
- **Path:** `/payment/images`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Payment Images](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PaymentId` | query | `string` | yes | Payment ID to fetch images for. |
| `ImageType` | query | `list<string>` | yes | Image type to return for the payment. |
