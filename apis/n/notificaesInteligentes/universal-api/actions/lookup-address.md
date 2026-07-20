# Notificações Inteligentes: Lookup Address

Retrieves an address from Notificações Inteligentes by postal code.

```
GET https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/lookup-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notificações Inteligentes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/lookup-address?connectionId=$CONNECTION_ID&postalCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postalCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notificaesInteligentes/latest/actions/lookup-address?${params}`, {
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
| `postalCode` | string | yes | The postal code to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |

## Native endpoint

Through the native Notificações Inteligentes API, this operation is `GET /addresses/:postalCode` (base URL `https://api.notificacoesinteligentes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-address.md) for the provider-specific parameters and requirements.

