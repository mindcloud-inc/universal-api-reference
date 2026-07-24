# Download Payment Image with Rillion Prime Pay

## Endpoint

- **Method:** `GET`
- **Path:** `/payment/images/download`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Download Payment Image](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageUrl` | query | `string` | yes | Use the full image URL returned by List Payment Images for check images. |
