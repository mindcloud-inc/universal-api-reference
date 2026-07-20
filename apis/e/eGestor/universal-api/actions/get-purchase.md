# eGestor: Get Purchase

Retrieves details for a purchase from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-purchase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-purchase?connectionId=$CONNECTION_ID&codigo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "codigo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-purchase?${params}`, {
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
| `codigo` | number | yes | Código da compra. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ativo": 1,
      "codCompraXML": 1,
      "codContato": 1,
      "codigo": 1,
      "dtCad": "2026-05-07T12:00:00.000Z",
      "dtCompra": "2026-05-07T12:00:00.000Z",
      "dtEntrega": "2026-05-07T12:00:00.000Z",
      "extDesp": 1,
      "extFrete": 1,
      "extST": 1,
      "financeiros": [
        {
          "codBoleto": 1,
          "codCaixa": 1,
          "codigo": 1,
          "codRecibo": 1,
          "descricao": "string",
          "dtComp": "2026-05-07T12:00:00.000Z",
          "dtVenc": "2026-05-07T12:00:00.000Z",
          "situacao": 1,
          "valor": 1
        }
      ],
      "nomeContato": "string",
      "numNota": "string",
      "obs": "string",
      "produtos": [
        {
          "codigo": 1,
          "codigoProprio": "string",
          "codProduto": 1,
          "custoBruto": 1,
          "custoCadProd": 1,
          "descricao": "string",
          "obs": "string",
          "quant": 1,
          "valorIPI": 1,
          "valorST": 1,
          "vDesc": 1
        }
      ],
      "situacao": 1,
      "valorTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ativo` | number |  |
| `codCompraXML` | number |  |
| `codContato` | number |  |
| `codigo` | number |  |
| `dtCad` | date |  |
| `dtCompra` | date |  |
| `dtEntrega` | date |  |
| `extDesp` | number |  |
| `extFrete` | number |  |
| `extST` | number |  |
| `financeiros[].codBoleto` | number |  |
| `financeiros[].codCaixa` | number |  |
| `financeiros[].codigo` | number |  |
| `financeiros[].codRecibo` | number |  |
| `financeiros[].descricao` | string |  |
| `financeiros[].dtComp` | date |  |
| `financeiros[].dtVenc` | date |  |
| `financeiros[].situacao` | number |  |
| `financeiros[].valor` | number |  |
| `nomeContato` | string |  |
| `numNota` | string |  |
| `obs` | string |  |
| `produtos[].codigo` | number |  |
| `produtos[].codigoProprio` | string |  |
| `produtos[].codProduto` | number |  |
| `produtos[].custoBruto` | number |  |
| `produtos[].custoCadProd` | number |  |
| `produtos[].descricao` | string |  |
| `produtos[].obs` | string |  |
| `produtos[].quant` | number |  |
| `produtos[].valorIPI` | number |  |
| `produtos[].valorST` | number |  |
| `produtos[].vDesc` | number |  |
| `situacao` | number |  |
| `valorTotal` | number |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /compras/:codigo` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase.md) for the provider-specific parameters and requirements.

