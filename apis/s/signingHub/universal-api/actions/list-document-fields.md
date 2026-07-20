# SigningHub: List Document Fields

Retrieves document fields from SigningHub.

```
GET https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/list-document-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/list-document-fields?connectionId=$CONNECTION_ID&documentId=1&packageId=1&pageNo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "1",
  "packageId": "1",
  "pageNo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/list-document-fields?${params}`, {
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
| `documentId` | number | yes | The ID of the document whose fields are requested. |
| `packageId` | number | yes | The ID of the package to which the document belongs. |
| `pageNo` | number | yes | Page number of the document whose fields are requested. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachment": [
        {}
      ],
      "checkbox": [
        {}
      ],
      "comment": [
        {}
      ],
      "dropdown": [
        {}
      ],
      "signature": [
        {}
      ],
      "text": [
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
| `attachment` | array<object> |  |
| `checkbox` | array<object> |  |
| `comment` | array<object> |  |
| `dropdown` | array<object> |  |
| `signature` | array<object> |  |
| `text` | array<object> |  |

## Native endpoint

Through the native SigningHub API, this operation is `GET /v4/packages/:packageId/documents/:documentId/fields/:pageNo` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-fields.md) for the provider-specific parameters and requirements.

