# Affinda: Get a document type

Retrieves a specific document type from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-document-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-document-type?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-document-type?${params}`, {
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
| `identifier` | string | yes | Document type identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "identifier": "string",
      "ingest_email": "ava@example.com",
      "name": "Ava Chen",
      "organization": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `identifier` | string |  |
| `ingest_email` | string |  |
| `name` | string |  |
| `organization` | string |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/document_types/:identifier` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-type.md) for the provider-specific parameters and requirements.

