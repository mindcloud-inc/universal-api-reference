# Add Envelope Annotation with Sign.Plus

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope/:envelope_id/annotation`
- **Base URL:** `https://restapi.sign.plus/v2`
- **Official documentation:** [Add Envelope Annotation](https://apidoc.sign.plus/api-reference/endpoints/signplus/add-envelope-annotation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes | — |
| `recipient_id` | body | `string` | yes | — |
| `document_id` | body | `string` | yes | — |
| `page` | body | `number` | yes | — |
| `x` | body | `number` | yes | — |
| `y` | body | `number` | yes | — |
| `width` | body | `number` | yes | — |
| `height` | body | `number` | yes | — |
| `required` | body | `boolean` | yes | — |
| `type` | body | `string` | yes | — |
| `text` | body | `object` | no | — |
| `signature` | body | `object` | no | JSON object for SIGNATURE annotations, for example {"id":""} |
| `initials` | body | `object` | no | JSON object for INITIALS annotations |
| `datetime` | body | `object` | no | JSON object for DATETIME annotations |
| `checkbox` | body | `object` | no | JSON object for CHECKBOX annotations |
