# Create Authentication Requirement with Clicksign

Creates an authentication requirement in Clicksign.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelopes/:envelope_id/requirements`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Create Authentication Requirement](https://developers.clicksign.com/reference/criar-requisito-de-autenticacao)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | JSON:API document wrapper. |
| `data.attributes` | body | `object` | no | Requirement attributes. |
| `data.attributes.auth` | body | `string` | yes | The authentication method. |
| `data.relationships` | body | `object` | no | Requirement relationships. |
| `data.relationships.document` | body | `object` | no | Target document relationship. |
| `data.relationships.document.data` | body | `object` | no | JSON:API document relationship wrapper. |
| `data.relationships.document.data.id` | body | `string` | yes | The UUID of the related document. |
| `data.relationships.signer` | body | `object` | no | Target signer relationship. |
| `data.relationships.signer.data` | body | `object` | no | JSON:API signer relationship wrapper. |
| `data.relationships.signer.data.id` | body | `string` | yes | The UUID of the related signer. |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
