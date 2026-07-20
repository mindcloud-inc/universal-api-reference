# Kit: List Forms

Lists forms in your Kit account.

```
GET https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-forms?${params}`, {
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
| `status` | list | no | Filter forms by status. One of: `active`, `all`, `inactive`. |
| `type` | list | no | Filter forms by type (embed or hosted). One of: `embed`, `hosted`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | string | no | Return results after this cursor. Example: `cursor_token`. |
| `before` | string | no | Return results before this cursor. Example: `cursor_token`. |
| `includeTotalCount` | boolean | no | Include total_count in pagination metadata. |
| `perPage` | number | no | Number of results per page. Example: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "forms": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `forms` | array<object> | List of forms returned by Kit. |
| `pagination` | object | Cursor pagination metadata. |

## Native endpoint

Through the native Kit API, this operation is `GET /forms` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

