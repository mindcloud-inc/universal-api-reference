# Ortto: Get Email Suppression List



```
GET https://connect.mindcloud.co/v1/universal/ortto/latest/actions/get-email-suppression-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/get-email-suppression-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ortto/latest/actions/get-email-suppression-list?${params}`, {
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
| `limit` | number | no | Maximum number of suppression-list emails to return (1-500). |
| `offset` | number | no | Number of suppression-list records to skip before returning results. |
| `sortOrder` | string | no | Sort order for suppression-list results: asc or desc. |
| `sort` | string | no | Field to sort by. Ortto documents email for this endpoint. |
| `includeEmails[]` | array<string> | no | Specific email addresses to include in the suppression-list response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "meta": {
        "total": 1,
        "totalActive": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean |  |
| `meta.total` | number |  |
| `meta.totalActive` | number |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /suppression-list/email/get` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-suppression-list.md) for the provider-specific parameters and requirements.

