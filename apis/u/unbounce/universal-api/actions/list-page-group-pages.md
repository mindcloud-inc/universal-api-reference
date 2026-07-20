# Unbounce: List Page Group Pages

Retrieves pages for an Unbounce page group.

```
GET https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-page-group-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unbounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-page-group-pages?connectionId=$CONNECTION_ID&page_group_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page_group_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-page-group-pages?${params}`, {
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
| `page_group_id` | string | yes | Unbounce page group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "pages": [
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
| `metadata` | object | Collection metadata from the Unbounce example response, including count, documentation, location, and related links. |
| `pages` | array<object> | Array of page objects from the Unbounce example response for the page group. |

## Native endpoint

Through the native Unbounce API, this operation is `GET /page_groups/:page_group_id/pages` (base URL `https://api.unbounce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-page-group-pages.md) for the provider-specific parameters and requirements.

