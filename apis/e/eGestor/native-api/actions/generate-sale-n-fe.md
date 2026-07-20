# Generate Sale NFe with eGestor

Generates an NFe for a sale in eGestor.

## Endpoint

- **Method:** `POST`
- **Path:** `/vendas/:codigo/gerarNfe`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Generate Sale NFe](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L4137)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codigo` | path | `number` | yes | Código da venda. |
| `enviar` | body | `boolean` | no | Define se a nota deve ser enviada à SEFAZ. |
| `contigOffline` | body | `boolean` | no | Define se a emissão será em contingência offline. |
