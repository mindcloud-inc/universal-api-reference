# Kit: List Form Subscribers

Lists subscribers for a Kit form.

```
GET https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-form-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-form-subscribers?connectionId=$CONNECTION_ID&limit=25&offset=0&formId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "formId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-form-subscribers?${params}`, {
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
| `formId` | number | yes | The ID of the form. Example: `12345`. |
| `status` | list | no | Filter subscribers by status. One of: `active`, `all`, `bounced`, `cancelled`, `complained`, `inactive`. |
| `emailAddress` | string | no | Filter by exact email address. Example: `subscriber@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addedAfter` | date | no | Filter subscribers added after this timestamp. |
| `addedBefore` | date | no | Filter subscribers added before this timestamp. |
| `createdAfter` | date | no | Filter subscribers created after this timestamp. |
| `createdBefore` | date | no | Filter subscribers created before this timestamp. |
| `after` | string | no | Return results after this cursor. Example: `cursor_token`. |
| `before` | string | no | Return results before this cursor. Example: `cursor_token`. |
| `includeTotalCount` | boolean | no | Include total_count in pagination metadata. |
| `perPage` | number | no | Number of results per page. Example: `50`. |
| `sortOrder` | list | no | Sort order for results. One of: `asc`, `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "subscribers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object | Cursor pagination metadata. |
| `subscribers` | array<object> | List of subscribers for the form. |

## Native endpoint

Through the native Kit API, this operation is `GET /forms/:form_id/subscribers` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-form-subscribers.md) for the provider-specific parameters and requirements.

