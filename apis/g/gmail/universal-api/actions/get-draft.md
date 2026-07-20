# Google Mail: Get Draft

Retrieves a Gmail draft.

```
GET https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-draft?connectionId=$CONNECTION_ID&id=r-1845c1d2fa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "r-1845c1d2fa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-draft?${params}`, {
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
| `id` | string | yes | Draft ID to fetch. Example: `r-1845c1d2fa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": {
        "id": "string",
        "labelIds": [
          "string"
        ],
        "threadId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message.id` | string |  |
| `message.labelIds[]` | string |  |
| `message.threadId` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `GET /drafts/:id` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-draft.md) for the provider-specific parameters and requirements.

