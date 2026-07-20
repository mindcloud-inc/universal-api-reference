# Pappers: Get Beneficial Ownership Declaration



```
GET https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-beneficial-ownership-declaration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pappers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-beneficial-ownership-declaration?connectionId=$CONNECTION_ID&siren=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siren": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-beneficial-ownership-declaration?${params}`, {
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
| `siren` | string | yes | French company SIREN identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Pappers API, this operation is `GET /document/declaration_beneficiaires_effectifs` (base URL `https://api.pappers.fr/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-beneficial-ownership-declaration.md) for the provider-specific parameters and requirements.

