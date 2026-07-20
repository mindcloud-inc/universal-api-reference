# Search Envelopes By Reference with edatalia Sign Online

Finds envelopes in edatalia Sign Online by external reference.

## Endpoint

- **Method:** `GET`
- **Path:** `/PSC/v40/DocumentSet/InfoByReference/:documentSetReference`
- **Base URL:** `https://restapi.firmar.online`
- **Official documentation:** [Search Envelopes By Reference](https://restapi.firmar.online/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentSetReference` | path | `string` | yes | External envelope reference to search for. |
