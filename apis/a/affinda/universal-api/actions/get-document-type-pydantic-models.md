# Affinda: Generate Pydantic models from a document type

Retrieves Pydantic models for an Affinda document type.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-document-type-pydantic-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-document-type-pydantic-models?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-document-type-pydantic-models?${params}`, {
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
| `identifier` | string | yes | Document type's identifier |
| `modelName` | string | no | Name for the Pydantic model |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/document_types/:identifier/pydantic_models` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-type-pydantic-models.md) for the provider-specific parameters and requirements.

