# Ugosign: Get Contract Custom Vars

Retrieves a contract's custom variables from Ugosign.

```
GET https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-contract-custom-vars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ugosign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-contract-custom-vars?connectionId=$CONNECTION_ID&contract=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contract": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-contract-custom-vars?${params}`, {
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
| `contract` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "slug": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `slug` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Ugosign API, this operation is `GET /v1/contracts/:contract/customVars` (base URL `https://app.ugosign.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contract-custom-vars.md) for the provider-specific parameters and requirements.

