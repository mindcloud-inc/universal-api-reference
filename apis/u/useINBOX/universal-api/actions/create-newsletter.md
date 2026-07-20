# UseINBOX: Create Newsletter

Creates a newsletter in UseINBOX.

```
POST https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-newsletter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-newsletter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "language": "en-US",
  "htmlContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-newsletter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "language": "en-US",
    "htmlContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | Newsletter subject. |
| `language` | string | yes | Newsletter language code such as en-US. Default: `en-US`. |
| `htmlContent` | string | yes | Newsletter HTML content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "htmlContent": "string",
      "id": "string",
      "language": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `htmlContent` | string |  |
| `id` | string |  |
| `language` | string |  |
| `subject` | string |  |

## Native endpoint

Through the native UseINBOX API, this operation is `POST /inbox/v1/newsletters` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-newsletter.md) for the provider-specific parameters and requirements.

