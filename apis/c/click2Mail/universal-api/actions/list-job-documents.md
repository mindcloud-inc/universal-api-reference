# Click2Mail: List Job Documents

Retrieves a list of job documents from Click2Mail.

```
GET https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/list-job-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/list-job-documents?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/list-job-documents?${params}`, {
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
| `documentId` | string | yes | The document id |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offset` | number | no | offset from beginning to allow you to paginate through the documents |
| `numberOfDocuments` | number | no | number of documents to return |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Click2Mail API, this operation is `GET /molpro/documents/jobDocuments` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-documents.md) for the provider-specific parameters and requirements.

