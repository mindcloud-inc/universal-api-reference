# eGestor: Get Sale

Retrieves details for a sale from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-sale?connectionId=$CONNECTION_ID&codigo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "codigo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-sale?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codigo` | number | yes | Código da venda. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listarCanceladas` | boolean | no | Define se vendas canceladas também podem ser detalhadas. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ativo": true,
      "clienteFinal": true,
      "codContato": 1,
      "codigo": 1,
      "codVendedor": 1,
      "dtCad": "2026-05-07T12:00:00.000Z",
      "dtEntrega": "2026-05-07T12:00:00.000Z",
      "dtVenda": "2026-05-07T12:00:00.000Z",
      "financeiros": [
        {
          "codBoleto": 1,
          "codCaixa": 1,
          "codFormaPgto": 1,
          "codigo": 1,
          "codPlanoContas": 1,
          "codRecibo": 1,
          "descricao": "string",
          "dtComp": "2026-05-07T12:00:00.000Z",
          "dtVenc": "2026-05-07T12:00:00.000Z",
          "nomeFormaPgto": "string",
          "situacao": 1,
          "valor": 1
        }
      ],
      "nomeContato": "string",
      "nomeVendedor": "string",
      "numParcelas": 1,
      "produtos": [
        {
          "codigo": 1,
          "codigoProprio": "string",
          "codProduto": 1,
          "custo": 1,
          "custoCadProd": 1,
          "descricao": "string",
          "obs": "string",
          "preco": 1,
          "quant": 1,
          "tipo": "string",
          "valorCOFINSST": 1,
          "valorFCPST": 1,
          "valorIPI": 1,
          "valorPISST": 1,
          "valorST": 1,
          "vDesc": 1
        }
      ],
      "publicURL": "https://example.com",
      "situacao": 1,
      "situacaoOS": "string",
      "valorEntrada": 1,
      "valorFinanc": 1,
      "valorFrete": 1,
      "valorTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ativo` | boolean |  |
| `clienteFinal` | boolean |  |
| `codContato` | number |  |
| `codigo` | number |  |
| `codVendedor` | number |  |
| `dtCad` | date |  |
| `dtEntrega` | date |  |
| `dtVenda` | date |  |
| `financeiros[].codBoleto` | number |  |
| `financeiros[].codCaixa` | number |  |
| `financeiros[].codFormaPgto` | number |  |
| `financeiros[].codigo` | number |  |
| `financeiros[].codPlanoContas` | number |  |
| `financeiros[].codRecibo` | number |  |
| `financeiros[].descricao` | string |  |
| `financeiros[].dtComp` | date |  |
| `financeiros[].dtVenc` | date |  |
| `financeiros[].nomeFormaPgto` | string |  |
| `financeiros[].situacao` | number |  |
| `financeiros[].valor` | number |  |
| `nomeContato` | string |  |
| `nomeVendedor` | string |  |
| `numParcelas` | number |  |
| `produtos[].codigo` | number |  |
| `produtos[].codigoProprio` | string |  |
| `produtos[].codProduto` | number |  |
| `produtos[].custo` | number |  |
| `produtos[].custoCadProd` | number |  |
| `produtos[].descricao` | string |  |
| `produtos[].obs` | string |  |
| `produtos[].preco` | number |  |
| `produtos[].quant` | number |  |
| `produtos[].tipo` | string |  |
| `produtos[].valorCOFINSST` | number |  |
| `produtos[].valorFCPST` | number |  |
| `produtos[].valorIPI` | number |  |
| `produtos[].valorPISST` | number |  |
| `produtos[].valorST` | number |  |
| `produtos[].vDesc` | number |  |
| `publicURL` | string |  |
| `situacao` | number |  |
| `situacaoOS` | string |  |
| `valorEntrada` | number |  |
| `valorFinanc` | number |  |
| `valorFrete` | number |  |
| `valorTotal` | number |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /vendas/:codigo` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sale.md) for the provider-specific parameters and requirements.

