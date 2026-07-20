# OpenRegister: Autocomplete Companies

Finds company matches in OpenRegister as you type.

```
GET https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/autocomplete-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRegister `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/autocomplete-companies?connectionId=$CONNECTION_ID&query=Siemens" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "Siemens"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/autocomplete-companies?${params}`, {
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
| `query` | string | yes | Text search query to find companies by name. Example: `Siemens`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Companies matching the autocomplete query. |

## Native endpoint

Through the native OpenRegister API, this operation is `GET /v1/autocomplete/company` (base URL `https://api.openregister.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-companies.md) for the provider-specific parameters and requirements.

