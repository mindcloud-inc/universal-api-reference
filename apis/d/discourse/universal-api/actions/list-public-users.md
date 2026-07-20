# Discourse: List Public Users

Retrieves public forum users from Discourse.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-public-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-public-users?connectionId=$CONNECTION_ID&order=string&period=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "order": "string",
  "period": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-public-users?${params}`, {
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
| `asc` | string | no | Set to true to sort ascending when supported. |
| `order` | string | yes | Directory sort field such as likes_received or post_count. |
| `page` | string | no | Directory page number. |
| `period` | string | yes | Directory period such as daily, weekly, monthly, quarterly, yearly, or all. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "directory_items": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directory_items` | array<object> |  |
| `meta` | object |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /directory_items.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-users.md) for the provider-specific parameters and requirements.

