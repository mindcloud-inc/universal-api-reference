# Generate Bacon Ipsum with Bacon Ipsum

## Endpoint

- **Method:** `GET`
- **Path:** `/api/`
- **Base URL:** `https://baconipsum.com`
- **Official documentation:** [Generate Bacon Ipsum](https://baconipsum.com/json-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Text type: all-meat or meat-and-filler. |
| `paras` | query | `string` | no | Number or range of paragraphs; defaults to 5 unless sentences is set. |
| `sentences` | query | `string` | no | Number of sentences; overrides paragraphs. |
| `start-with-lorem` | query | `string` | no | Pass 1 to start the first paragraph with Bacon ipsum dolor sit amet. |
