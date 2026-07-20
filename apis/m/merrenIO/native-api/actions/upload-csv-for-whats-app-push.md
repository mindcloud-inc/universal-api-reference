# Upload CSV For WhatsApp Push with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/deploy/uploadRecipients`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Upload CSV For WhatsApp Push](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey receiving the WhatsApp push upload. |
| `csvFile` | body | `string` | yes | CSV payload or file token containing WhatsApp recipients. |
