# Devin: List Session Attachments

Retrieves session attachments from a Devin session.

```
GET https://connect.mindcloud.co/v1/universal/devin/latest/actions/list-session-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devin/latest/actions/list-session-attachments?connectionId=$CONNECTION_ID&devinId=string&orgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "devinId": "string",
  "orgId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devin/latest/actions/list-session-attachments?${params}`, {
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
| `devinId` | string | yes | Session ID prefixed with devin-. |
| `orgId` | string | yes | Devin organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end_cursor": "string",
      "has_next_page": true,
      "items": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end_cursor` | string | Cursor for the next page. |
| `has_next_page` | boolean | Whether more results are available. |
| `items` | array<object> | Session attachments returned by Devin. |
| `total` | number | Total count when returned by Devin. |

## Native endpoint

Through the native Devin API, this operation is `GET /v3/organizations/:org_id/sessions/:devin_id/attachments` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-session-attachments.md) for the provider-specific parameters and requirements.

