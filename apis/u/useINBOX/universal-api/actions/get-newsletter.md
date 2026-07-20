# UseINBOX: Get Newsletter

Retrieves a newsletter from UseINBOX.

```
GET https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-newsletter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-newsletter?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-newsletter?${params}`, {
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
| `id` | string | yes | Newsletter ID from INBOX. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "2026-05-07T12:00:00.000Z",
      "htmlContent": "string",
      "id": "string",
      "language": "string",
      "subject": "string",
      "updateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | date |  |
| `htmlContent` | string |  |
| `id` | string |  |
| `language` | string |  |
| `subject` | string |  |
| `updateTime` | date |  |

## Native endpoint

Through the native UseINBOX API, this operation is `GET /inbox/v1/newsletters/:id` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-newsletter.md) for the provider-specific parameters and requirements.

