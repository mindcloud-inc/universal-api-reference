# DigiParser: Delete Documents



```
DELETE https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/delete-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DigiParser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/delete-documents?connectionId=$CONNECTION_ID&parserId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parserId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/delete-documents?${params}`, {
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
| `parserId` | string | yes | Parser UUID from DigiParser Parser Settings -> General Settings. |
| `documentIds[]` | array<string> | no | Optional list of document UUIDs to delete. |
| `externalIds[]` | array<string> | no | Optional list of external IDs to delete documents by external ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": 1,
      "ids": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | number | Count of documents affected by the delete request. |
| `ids` | array<string> | Document UUIDs reported by DigiParser for the delete operation. |
| `success` | boolean | Whether the delete request succeeded. |

## Native endpoint

Through the native DigiParser API, this operation is `POST /api/v1/process/:parserId/documents/delete` (base URL `https://app.digiparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-documents.md) for the provider-specific parameters and requirements.

