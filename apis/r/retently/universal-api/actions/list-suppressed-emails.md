# Retently: List Suppressed Emails

Retrieves a list of suppressed emails from Retently.

```
GET https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-suppressed-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-suppressed-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-suppressed-emails?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "addedBy": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "id": "string",
      "note": "string",
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedBy` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `id` | string |  |
| `note` | string |  |
| `reason` | string |  |

## Native endpoint

Through the native Retently API, this operation is `GET /api/v2/suppressions/emails` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-suppressed-emails.md) for the provider-specific parameters and requirements.

