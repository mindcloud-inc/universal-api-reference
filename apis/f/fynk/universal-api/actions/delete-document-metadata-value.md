# fynk: Delete Document Metadata Value

Deletes a document metadata value from fynk.

```
DELETE https://connect.mindcloud.co/v1/universal/fynk/latest/actions/delete-document-metadata-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fynk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fynk/latest/actions/delete-document-metadata-value?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fynk/latest/actions/delete-document-metadata-value?${params}`, {
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
| `document` | string | no | Document UUID. Default: `25c718b2-be8b-44e7-858f-3152e7380022`. |
| `metadataValue` | string | no | Metadata value UUID. Default: `ed838e33-022e-4c58-8549-5cab7026e49c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native fynk API, this operation is `DELETE /documents/:document/metadata-values/:metadataValue` (base URL `https://app.fynk.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document-metadata-value.md) for the provider-specific parameters and requirements.

