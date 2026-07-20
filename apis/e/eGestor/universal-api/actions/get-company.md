# eGestor: Get Company

Retrieves company details from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-company?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "atividade": 1,
      "bairro": "string",
      "baseCSLL": "string",
      "baseIRPJ": "string",
      "cep": "string",
      "cidadeCod": "string",
      "cidadeNome": "string",
      "cifrao": "string",
      "cmc": "string",
      "cnae": "string",
      "codTributMunicipio": "string",
      "compl": "string",
      "cpfcnpj": "string",
      "crt": 1,
      "emails": "ava@example.com",
      "end": "string",
      "fantasia": "string",
      "fones": "string",
      "inscEstadual": "string",
      "inscMunicipal": "string",
      "nome": "string",
      "num": "string",
      "pCOFINS": "string",
      "pCSLL": "string",
      "pICMS": "string",
      "pIRPJ": "string",
      "pPIS": "string",
      "pSimples": 1,
      "regimeTributacao": "string",
      "rntrc": "string",
      "tipoIE": "string",
      "uf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `atividade` | number |  |
| `bairro` | string |  |
| `baseCSLL` | string |  |
| `baseIRPJ` | string |  |
| `cep` | string |  |
| `cidadeCod` | string |  |
| `cidadeNome` | string |  |
| `cifrao` | string |  |
| `cmc` | string |  |
| `cnae` | string |  |
| `codTributMunicipio` | string |  |
| `compl` | string |  |
| `cpfcnpj` | string |  |
| `crt` | number |  |
| `emails` | string |  |
| `end` | string |  |
| `fantasia` | string |  |
| `fones` | string |  |
| `inscEstadual` | string |  |
| `inscMunicipal` | string |  |
| `nome` | string |  |
| `num` | string |  |
| `pCOFINS` | string |  |
| `pCSLL` | string |  |
| `pICMS` | string |  |
| `pIRPJ` | string |  |
| `pPIS` | string |  |
| `pSimples` | number |  |
| `regimeTributacao` | string |  |
| `rntrc` | string |  |
| `tipoIE` | string |  |
| `uf` | string |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /empresa` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

