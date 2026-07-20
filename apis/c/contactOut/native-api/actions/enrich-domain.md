# Enrich Domain with ContactOut

Retrieves company details for domain names in ContactOut.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/domain/enrich`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Enrich Domain](https://api.contactout.com/#company-information-from-domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domains` | body | `string` | yes | An array of company domains to enrich. Send multiple values as a array. |
