# Check VAT Registration with UK Check VAT

## Endpoint

- **Method:** `GET`
- **Path:** `/organisations/vat/check-vat-number/lookup/:targetVrn`
- **Base URL:** `https://test-api.service.hmrc.gov.uk`
- **Official documentation:** [Check VAT Registration](https://raw.githubusercontent.com/hmrc/vat-registered-companies-api/main/public/api/conf/2.0/application.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetVrn` | path | `string` | yes | UK VAT registration number to check. HMRC accepts a 9-digit or 12-digit number. |
