# MailerCheck: Get Verification List Results

Retrieves verification results for a list from MailerCheck.

```
GET https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-verification-list-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-verification-list-results?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-verification-list-results?${params}`, {
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
| `id` | number | yes | Verification list identifier. |
| `result` | string | no | Filter results by verification outcome. |
| `limit` | number | no | Maximum number of result rows to return. |
| `page` | number | no | Results page number. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "checked": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "result": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `checked` | number |  |
| `createdAt` | date |  |
| `id` | number |  |
| `result` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native MailerCheck API, this operation is `GET /lists/:id/results` (base URL `https://app.mailercheck.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification-list-results.md) for the provider-specific parameters and requirements.

