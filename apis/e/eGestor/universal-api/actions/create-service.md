# eGestor: Create Service

Creates a new service in eGestor.

```
POST https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "descricao": "MindCloud Stage3 Service 20260401"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-service', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "descricao": "MindCloud Stage3 Service 20260401"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `descricao` | string | yes | Descrição do serviço. Example: `MindCloud Stage3 Service 20260401`. |
| `precoVenda` | number | no | Preço de venda. Example: `10`. |
| `codigoGrupoTributos` | number | no | Código do grupo de tributos vinculado. Example: `0`. |
| `itemListaServico` | string | no | Código do item da lista de serviço. Example: `14.01`. |
| `cnae` | string | no | Código CNAE. Example: `1234567`. |
| `codTributacaoMun` | string | no | Código de tributação municipal. Example: `987654`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `anotacoesInternas` | string | no | Anotações internas do serviço. Example: `Anotação`. |
| `tags[]` | array<string> | no | Lista de tags do serviço. Example: `Exemplo,API`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codigo": 1,
      "descricao": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codigo` | number |  |
| `descricao` | string |  |

## Native endpoint

Through the native eGestor API, this operation is `POST /servicos` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service.md) for the provider-specific parameters and requirements.

