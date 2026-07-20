# Harbour: Get Document

Retrieves a specific document from Harbour.

```
GET https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-document?connectionId=$CONNECTION_ID&document_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-document?${params}`, {
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
| `document_id` | string | yes | ID of the document to retrieve. |
| `version_number` | number | no | Specific document version to retrieve. Omit to fetch the latest version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document` | object |  |

## Native endpoint

Through the native Harbour API, this operation is `GET /documents/:document_id` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

