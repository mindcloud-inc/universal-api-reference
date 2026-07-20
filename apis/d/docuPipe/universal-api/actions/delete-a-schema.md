# DocuPipe: Delete a Schema

Deletes a schema from DocuPipe.

```
DELETE https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/delete-a-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/delete-a-schema?connectionId=$CONNECTION_ID&schemaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schemaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/delete-a-schema?${params}`, {
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
| `schemaId` | string | yes |  |

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
| `success` | boolean | Whether the deletion was successful or not. |

## Native endpoint

Through the native DocuPipe API, this operation is `DELETE /schema/:schemaId` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-schema.md) for the provider-specific parameters and requirements.

