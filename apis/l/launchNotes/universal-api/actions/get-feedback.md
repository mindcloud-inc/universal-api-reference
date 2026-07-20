# LaunchNotes: Get Feedback



```
GET https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-feedback?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-feedback?${params}`, {
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
| `id` | string | yes | Feedback identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affectedCustomerEmail": "ava@example.com",
      "archived": true,
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affectedCustomerEmail` | string | Customer email tied to the feedback. |
| `archived` | boolean | Whether the feedback is archived. |
| `content` | string | Feedback content. |
| `createdAt` | date | Feedback creation timestamp. |
| `id` | string | Feedback identifier. |
| `updatedAt` | date | Feedback update timestamp. |

## Native endpoint

Through the native LaunchNotes API, this operation is `POST /graphql` (base URL `https://app.launchnotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feedback.md) for the provider-specific parameters and requirements.

