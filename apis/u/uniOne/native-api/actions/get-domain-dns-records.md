# Get Domain DNS Records with UniOne

Retrieves domain DNS records from UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `domain/get-dns-records.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Get Domain DNS Records](https://docs.unione.io/en/web-api-ref#domain-get-dns-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Domain name to inspect. |
