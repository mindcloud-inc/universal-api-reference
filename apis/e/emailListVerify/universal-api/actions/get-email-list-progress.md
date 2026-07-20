# EmailListVerify: Get Email List Progress

Retrieves email list verification progress from EmailListVerify.

```
GET https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-email-list-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailListVerify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-email-list-progress?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-email-list-progress?${params}`, {
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
| `id` | string | yes | Uploaded email list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "credits": {
        "charged": 1,
        "returned": 1
      },
      "name": "Ava Chen",
      "progress": 1,
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Upload timestamp. |
| `credits` | object | Credit accounting for the email list. |
| `credits.charged` | number | Credits charged. |
| `credits.returned` | number | Credits returned. |
| `name` | string | Uploaded file name. |
| `progress` | number | Completion percentage. |
| `status` | string | Email list status. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native EmailListVerify API, this operation is `GET /api/maillists/:id/progress` (base URL `https://api.emaillistverify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-list-progress.md) for the provider-specific parameters and requirements.

