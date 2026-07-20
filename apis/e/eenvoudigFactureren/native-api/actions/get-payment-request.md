# Get Payment Request with EenvoudigFactureren

Retrieves a payment request from EenvoudigFactureren.

## Endpoint

- **Method:** `GET`
- **Path:** `/paymentrequests/:paymentrequest_id`
- **Base URL:** `https://eenvoudigfactureren.be/api/v1`
- **Official documentation:** [Get Payment Request](https://help.eenvoudigfactureren.be/support/solutions/articles/101000448907-api-betaalverzoeken)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentrequest_id` | path | `string` | yes | EenvoudigFactureren payment request ID. |
