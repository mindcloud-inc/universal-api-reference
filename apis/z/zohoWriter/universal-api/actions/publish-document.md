# Zoho Writer: Publish Document

Publishes a document in Zoho Writer.

```
PUT https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/publish-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/publish-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scope": "organization"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/publish-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scope": "organization"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scope` | string | yes | Publish scope. Use organization to publish within the org or external to publish publicly. Default: `organization`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": "string",
      "scope": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `result` | string |  |
| `scope` | string |  |

## Native endpoint

Through the native Zoho Writer API, this operation is `POST /v1/documents/:document_id/publish` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-document.md) for the provider-specific parameters and requirements.

