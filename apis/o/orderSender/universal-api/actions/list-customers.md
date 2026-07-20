# Order Sender: List Customers

Retrieves customer records from Order Sender.

```
GET https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-customers?${params}`, {
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
| `delimiter` | string | no | Delimiter used only when requesting CSV output. |
| `format` | string | no | Response format. Use json for structured records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cap": "string",
      "categoria": "string",
      "cellulare": "string",
      "citta": "string",
      "codice": "string",
      "codice_agente_associato": "string",
      "codice_listini": "string",
      "codice_sdi": "string",
      "codicefiscale": "string",
      "email": "ava@example.com",
      "email_pec": "ava@example.com",
      "fax": "string",
      "frequenza": "string",
      "giornochiusura": "string",
      "iban": "string",
      "indirizzo": "string",
      "lat": "string",
      "lng": "string",
      "modalita_consegna": "string",
      "nazione": "string",
      "nome": "string",
      "note": "string",
      "pagamento": "string",
      "partitaiva": "string",
      "provincia": "string",
      "ragione_sociale": "string",
      "responsabile": "string",
      "sito": "string",
      "telefono": "string",
      "zona": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cap` | string |  |
| `categoria` | string |  |
| `cellulare` | string |  |
| `citta` | string |  |
| `codice` | string |  |
| `codice_agente_associato` | string |  |
| `codice_listini` | string |  |
| `codice_sdi` | string |  |
| `codicefiscale` | string |  |
| `email` | string |  |
| `email_pec` | string |  |
| `fax` | string |  |
| `frequenza` | string |  |
| `giornochiusura` | string |  |
| `iban` | string |  |
| `indirizzo` | string |  |
| `lat` | string |  |
| `lng` | string |  |
| `modalita_consegna` | string |  |
| `nazione` | string |  |
| `nome` | string |  |
| `note` | string |  |
| `pagamento` | string |  |
| `partitaiva` | string |  |
| `provincia` | string |  |
| `ragione_sociale` | string |  |
| `responsabile` | string |  |
| `sito` | string |  |
| `telefono` | string |  |
| `zona` | string |  |

## Native endpoint

Through the native Order Sender API, this operation is `GET /op/export/res/clienti` (base URL `https://business.ordersender.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

