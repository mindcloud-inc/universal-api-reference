# Zoho Writer: Enable Or Disable Track Changes

Enables or disables track changes in Zoho Writer.

```
PUT https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/enable-or-disable-track-changes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/enable-or-disable-track-changes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "operations": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/enable-or-disable-track-changes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "operations": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | The unique ID of the Zoho Writer document. |
| `operations` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": "string"
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

## Native endpoint

Through the native Zoho Writer API, this operation is `POST /v1/documents/:document_id/meta` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enable-or-disable-track-changes.md) for the provider-specific parameters and requirements.

