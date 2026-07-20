# Qive: Get Received NFSe Manual PDF



```
GET https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-received-nfse-manual-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-received-nfse-manual-pdf?connectionId=$CONNECTION_ID&id=string&cnpj=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "cnpj": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-received-nfse-manual-pdf?${params}`, {
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
| `id` | string | yes | NFSe identifier for the original received manual PDF. |
| `cnpj` | string | yes | Owner CNPJ for the original received manual PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pdf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pdf` | string |  |

## Native endpoint

Through the native Qive API, this operation is `GET /v1/nfse/received/manual/pdf` (base URL `https://sandbox-api.arquivei.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-received-nfse-manual-pdf.md) for the provider-specific parameters and requirements.

