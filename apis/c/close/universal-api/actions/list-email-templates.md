# Close: List Email Templates

Retrieves email templates from Close.

```
GET https://connect.mindcloud.co/v1/universal/close/latest/actions/list-email-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Close `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/close/latest/actions/list-email-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/close/latest/actions/list-email-templates?${params}`, {
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
| `isArchived` | boolean | no | Filter archived templates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "hasMore": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Email template results. |
| `hasMore` | boolean | Whether more records are available. |

## Native endpoint

Through the native Close API, this operation is `GET /email_template/` (base URL `https://api.close.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-email-templates.md) for the provider-specific parameters and requirements.

