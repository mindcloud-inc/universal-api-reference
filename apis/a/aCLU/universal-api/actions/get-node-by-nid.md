# ACLU: Get Node By NID

Retrieves a Torture Database node by numeric ID.

```
GET https://connect.mindcloud.co/v1/universal/aCLU/latest/actions/get-node-by-nid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ACLU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aCLU/latest/actions/get-node-by-nid?connectionId=$CONNECTION_ID&nid=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nid": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aCLU/latest/actions/get-node-by-nid?${params}`, {
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
| `nid` | number | yes | Numeric Drupal node ID (nid). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field_doc_date": [
        {}
      ],
      "field_doc_description": [
        {}
      ],
      "field_doc_draft": [
        {}
      ],
      "field_doc_foia": [
        {}
      ],
      "field_doc_handwritten_text": [
        {}
      ],
      "field_doc_id": [
        {}
      ],
      "field_doc_pdf": [
        {}
      ],
      "field_doc_release_date": [
        {}
      ],
      "field_doc_text": [
        {}
      ],
      "nid": 1,
      "path": "string",
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
| `field_doc_date` | array<object> |  |
| `field_doc_description` | array<object> |  |
| `field_doc_draft` | array<object> |  |
| `field_doc_foia` | array<object> |  |
| `field_doc_handwritten_text` | array<object> |  |
| `field_doc_id` | array<object> |  |
| `field_doc_pdf` | array<object> |  |
| `field_doc_release_date` | array<object> |  |
| `field_doc_text` | array<object> |  |
| `nid` | number |  |
| `path` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native ACLU API, this operation is `GET /fullnode/retrieve.json` (base URL `https://www.thetorturedatabase.org/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-node-by-nid.md) for the provider-specific parameters and requirements.

