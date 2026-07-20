# GoSquared: List Smart Groups

Retrieves people smart groups from GoSquared.

```
GET https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-smart-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoSquared `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-smart-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-smart-groups?${params}`, {
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
      "filters": [
        {}
      ],
      "id": "string",
      "Links": [
        {}
      ],
      "name": "Ava Chen",
      "prefs": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filters` | array<object> | Provider filter rules that define the smart group. |
| `id` | string | GoSquared smart group identifier. |
| `Links` | array<object> | Provider link metadata returned for related smart group resources. |
| `name` | string | Display name of the smart group. |
| `prefs` | object | Provider preferences returned for the smart group. |

## Native endpoint

Through the native GoSquared API, this operation is `GET people/v1/smartgroups` (base URL `https://api.gosquared.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-smart-groups.md) for the provider-specific parameters and requirements.

