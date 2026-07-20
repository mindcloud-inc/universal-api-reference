# Finalize Purchase with eGestor

Finalizes a purchase in eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/compras/:codigo/efetivar`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Finalize Purchase](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3416)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codigo` | path | `number` | yes | Código da compra. |
| `atualizarPrecoVenda` | query | `boolean` | no | Define se o preço de venda dos produtos será atualizado ao efetivar. |
