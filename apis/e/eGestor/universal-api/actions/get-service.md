# eGestor: Get Service

Retrieves details for a service from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-service?connectionId=$CONNECTION_ID&codigo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "codigo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-service?${params}`, {
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
| `codigo` | number | yes | Código do serviço. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anotacoesInternas": "string",
      "cnae": "string",
      "codigo": 1,
      "codigoGrupoTributos": 1,
      "codTributacaoMun": "string",
      "descricao": "string",
      "dtCad": "2026-05-07T12:00:00.000Z",
      "itemListaServico": "string",
      "precoVenda": 1,
      "tags": [
        "string"
      ],
      "tipoProduto": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anotacoesInternas` | string |  |
| `cnae` | string |  |
| `codigo` | number |  |
| `codigoGrupoTributos` | number |  |
| `codTributacaoMun` | string |  |
| `descricao` | string |  |
| `dtCad` | date |  |
| `itemListaServico` | string |  |
| `precoVenda` | number |  |
| `tags[]` | string |  |
| `tipoProduto` | string |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /servicos/:codigo` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service.md) for the provider-specific parameters and requirements.

