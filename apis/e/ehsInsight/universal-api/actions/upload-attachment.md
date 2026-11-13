# EHS Insight: Upload Attachment



```
POST https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/upload-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EHS Insight `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/upload-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/upload-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileName` | string | no | File name including its extension, such as document.pdf. Example: `document.pdf`. |
| `fileBytesBase64` | string | no | The file contents encoded as Base64, a text representation of the file's bytes. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentType` | string | no | Optional media type, such as application/pdf. Inferred from the file name extension when omitted. Example: `application/pdf`. |
| `rowUid` | string | no | Optional and not recommended for normal uploads. Supply only when migrating identical attachments between sandbox and production; otherwise let EHS Insight generate the identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EHS Insight API returns.

## Native endpoint

Through the native EHS Insight API, this operation is `POST /v6/attachment/add` (base URL `https://{{credentials.companyName}}.ehsinsight.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-attachment.md) for the provider-specific parameters and requirements.

