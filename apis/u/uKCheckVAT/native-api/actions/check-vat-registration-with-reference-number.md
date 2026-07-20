# Check VAT Registration With Reference Number with UK Check VAT

## Endpoint

- **Method:** `GET`
- **Path:** `/organisations/vat/check-vat-number/lookup/:targetVrn/:requesterVrn`
- **Base URL:** `https://test-api.service.hmrc.gov.uk`
- **Official documentation:** [Check VAT Registration With Reference Number](https://raw.githubusercontent.com/hmrc/vat-registered-companies-api/main/public/api/conf/2.0/application.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetVrn` | path | `string` | yes | UK VAT registration number to check. HMRC accepts a 9-digit or 12-digit number. |
| `requesterVrn` | path | `string` | yes | Your VAT registration number. HMRC accepts a 9-digit or 12-digit number and returns a consultation number when this requester is valid. |
