# Get Financial Account Current Balance with Conta Azul

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/conta-financeira/{id_conta_financeira}/saldo-atual`
- **Base URL:** `https://api-v2.contaazul.com`
- **Official documentation:** [Get Financial Account Current Balance](https://developers.contaazul.com/open-api-docs/financial-apis-openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_conta_financeira` | path | `string` | yes | Conta Azul financial account identifier from the path. |
