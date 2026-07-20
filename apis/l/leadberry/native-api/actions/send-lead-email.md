# Send Lead Email with Leadberry

## Endpoint

- **Method:** `POST`
- **Path:** `/data/sendLeadEmail`
- **Base URL:** `https://app.leadberry.com`
- **Official documentation:** [Send Lead Email](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Email address to send the Leadberry lead email to. |
| `visibleUrlId` | body | `string` | yes | Leadberry visible URL identifier for the target lead. |
| `date` | body | `date` | yes | Lead date associated with the email. |
| `source` | body | `string` | yes | Lead source string from Leadberry result data. |
| `country` | body | `string` | yes | Lead country value. |
| `landingPagePath` | body | `string` | yes | Landing page path visited by the lead. |
| `deepContacts` | body | `string` | no | JSON-stringified deep contacts payload when available. |
