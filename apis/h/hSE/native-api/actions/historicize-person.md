# Historicize Person with 4HSE

Updates an existing person in 4HSE by historicizing it.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/person/historicize/:id`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Historicize Person](https://docs.4hse.com/en/api/person/#operation-historicizePerson-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Person ID. |
| `date` | body | `date` | no | Historicization date. |
