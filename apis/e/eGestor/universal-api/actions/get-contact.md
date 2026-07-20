# eGestor: Get Contact

Retrieves details for a contact from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-contact?connectionId=$CONNECTION_ID&codigo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "codigo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-contact?${params}`, {
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
| `codigo` | number | yes | Código do contato. Example: `1`. |

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

Through the native eGestor API, this operation is `GET /contatos/:codigo` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

