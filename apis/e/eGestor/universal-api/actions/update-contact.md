# eGestor: Update Contact

Updates an existing contact in eGestor.

```
PUT https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "codigo": "1",
  "nome": "MindCloud Stage3 Contact Updated",
  "tipo[]": "cliente"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "codigo": "1",
    "nome": "MindCloud Stage3 Contact Updated",
    "tipo[]": "cliente"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codigo` | number | yes | Código do contato. Example: `1`. |
| `nome` | string | yes | Nome do contato. Limite 60 caracteres. Example: `MindCloud Stage3 Contact Updated`. |
| `tipo[]` | array<string> | yes | Tipos do contato como lista de strings. Valores documentados: cliente, fornecedor, transportadora. Example: `cliente`. |
| `nomeParaContato` | string | no | Nome para contato. Limite 60 caracteres. Example: `Automation Contact Updated`. |
| `emails[]` | array<string> | no | Lista de e-mails do contato. Example: `apps@mindcloud.co`. |
| `clienteFinal` | boolean | no | Define se o contato é cliente final. Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `obs` | string | no | Observações gerais do contato. Example: `Updated by Codex stage 3 batch`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bairro": "string",
      "bairroEntrega": "string",
      "cep": 1,
      "cepEntrega": 1,
      "cidade": "string",
      "cidadeEntrega": "string",
      "clienteFinal": true,
      "codIBGE": "string",
      "codIBGEEntrega": "string",
      "codigo": 1,
      "complemento": "string",
      "complementoEntrega": "string",
      "cpfcnpj": "string",
      "cpfCnpjEntrega": "string",
      "descrComemoracao": "string",
      "dtCad": "2026-05-07T12:00:00.000Z",
      "dtComemoracao": "string",
      "dtNasc": "string",
      "emails": [
        "ava@example.com"
      ],
      "emailsEntrega": "ava@example.com",
      "fantasia": "string",
      "fonesEntrega": "string",
      "indicadorIE": 1,
      "inscEstadualEntrega": "string",
      "inscricaoEstadual": "string",
      "inscricaoEstadualST": "string",
      "inscricaoMunicipal": "string",
      "logradouro": "string",
      "logradouroEntrega": "string",
      "nome": "string",
      "nomeParaContato": "string",
      "numero": "string",
      "numeroEntrega": 1,
      "obs": "string",
      "pais": "string",
      "pontoRefEntrega": "string",
      "suframa": "string",
      "tipo": [
        "string"
      ],
      "uf": "string",
      "ufEntrega": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bairro` | string |  |
| `bairroEntrega` | string |  |
| `cep` | number |  |
| `cepEntrega` | number |  |
| `cidade` | string |  |
| `cidadeEntrega` | string |  |
| `clienteFinal` | boolean |  |
| `codIBGE` | string |  |
| `codIBGEEntrega` | string |  |
| `codigo` | number |  |
| `complemento` | string |  |
| `complementoEntrega` | string |  |
| `cpfcnpj` | string |  |
| `cpfCnpjEntrega` | string |  |
| `descrComemoracao` | string |  |
| `dtCad` | date |  |
| `dtComemoracao` | string |  |
| `dtNasc` | string |  |
| `emails[]` | string |  |
| `emailsEntrega` | string |  |
| `fantasia` | string |  |
| `fonesEntrega` | string |  |
| `indicadorIE` | number |  |
| `inscEstadualEntrega` | string |  |
| `inscricaoEstadual` | string |  |
| `inscricaoEstadualST` | string |  |
| `inscricaoMunicipal` | string |  |
| `logradouro` | string |  |
| `logradouroEntrega` | string |  |
| `nome` | string |  |
| `nomeParaContato` | string |  |
| `numero` | string |  |
| `numeroEntrega` | number |  |
| `obs` | string |  |
| `pais` | string |  |
| `pontoRefEntrega` | string |  |
| `suframa` | string |  |
| `tipo[]` | string |  |
| `uf` | string |  |
| `ufEntrega` | string |  |

## Native endpoint

Through the native eGestor API, this operation is `PUT /contatos/:codigo` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

