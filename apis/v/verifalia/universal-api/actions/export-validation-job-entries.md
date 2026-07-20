# Verifalia: Export Validation Job Entries

Retrieves exported email validation entries from Verifalia.

```
GET https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/export-validation-job-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/export-validation-job-entries?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/export-validation-job-entries?${params}`, {
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
| `id` | string | yes | The Verifalia validation job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "contentType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | The exported validation entries payload in the negotiated response format. |
| `contentType` | string | The MIME type returned by the export response. |

## Native endpoint

Through the native Verifalia API, this operation is `GET /email-validations/{id}/entries` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-validation-job-entries.md) for the provider-specific parameters and requirements.

