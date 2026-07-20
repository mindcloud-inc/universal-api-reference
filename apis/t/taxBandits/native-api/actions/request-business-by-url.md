# Request Business by URL with TaxBandits

Retrieves a business request URL from TaxBandits.

## Endpoint

- **Method:** `GET`
- **Path:** `Business/RequestByURL`
- **Base URL:** `https://testapi.taxbandits.com/v1.7.3/`
- **Official documentation:** [Request Business by URL](https://developer.taxbandits.com/docs/business/requestbyurl/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cancelurl` | query | `string` | no | Redirect URL after cancel. |
| `formtype` | query | `string` | no | Target form type for the business request URL. |
| `payerref` | query | `string` | no | Payer reference used to generate the business URL. |
| `returnurl` | query | `string` | no | Redirect URL after successful completion. |
