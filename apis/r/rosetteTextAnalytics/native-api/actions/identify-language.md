# Identify Language with Rosette Text Analytics

## Endpoint

- **Method:** `POST`
- **Path:** `/language`
- **Base URL:** `https://api.rosette.com/rest/v1`
- **Official documentation:** [Identify Language](https://docs.babelstreet.com/en/index-en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Text to process. |
| `contentUri` | body | `string` | no | URI to accessible content. Mutually exclusive with content. |
| `options.multilingual` | body | `boolean` | no | If true, detect language regions in multilingual documents. |
| `options.koreanDialects` | body | `boolean` | no | If true, include Korean dialect detection options. |
