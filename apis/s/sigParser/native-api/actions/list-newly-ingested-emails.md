# List Newly Ingested Emails with SigParser

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Emails/Distinct`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [List Newly Ingested Emails](https://ipaas.sigparser.com/v1#get-api-emails-distinct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ingested_after` | query | `number` | yes | Return emails ingested after this ingestion key. |
