# eGestor: List Services

Retrieves a list of services from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-services?${params}`, {
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
| `filtro` | string | no | Busca a string informada nos campos código e descrição do serviço. Example: `MindCloud Stage3 Service 20260401`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Campos a retornar separados por vírgula. Example: `codigo,descricao,precoVenda`. |
| `orderBy` | string | no | Ordenação da listagem no formato campo,direção. Example: `descricao,asc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {
          "anotacoesInternas": "string",
          "cnae": "string",
          "codigo": 1,
          "codigoGrupoTributos": 1,
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
      "from": 1,
      "lastPage": 1,
      "nextPageUrl": {},
      "perPage": 1,
      "prevPageUrl": {},
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data[].anotacoesInternas` | string |  |
| `data[].cnae` | string |  |
| `data[].codigo` | number |  |
| `data[].codigoGrupoTributos` | number |  |
| `data[].descricao` | string |  |
| `data[].dtCad` | date |  |
| `data[].itemListaServico` | string |  |
| `data[].precoVenda` | number |  |
| `data[].tags[]` | string |  |
| `data[].tipoProduto` | string |  |
| `from` | number |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /servicos` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

