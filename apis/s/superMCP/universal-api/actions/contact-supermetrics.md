# SuperMCP: Contact Supermetrics



```
POST https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/contact-supermetrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperMCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/contact-supermetrics" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "subject": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/contact-supermetrics', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "subject": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Request type, such as feedback, support, or sales. |
| `subject` | string | yes | Contact request subject. |
| `message` | string | yes | Contact request message. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | no | Optional request category. |
| `dataSourceId` | string | no | Optional related Supermetrics data source ID. |
| `company` | string | no | Optional company name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Response message. |
| `success` | boolean | Whether contact request was accepted. |

## Native endpoint

Through the native SuperMCP API, this operation is `POST /mcp/contact_supermetrics` (base URL `https://mcp.supermetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/contact-supermetrics.md) for the provider-specific parameters and requirements.

