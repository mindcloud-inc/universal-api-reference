# Cerbo: List Vitals Tag Groups

Retrieves vitals tag groups from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-vitals-tag-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-vitals-tag-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-vitals-tag-groups?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "created_by": 1,
      "included_fields": [
        "string"
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `created_by` | number |  |
| `included_fields` | array<string> |  |
| `name` | string |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /vitals_tag_groups` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vitals-tag-groups.md) for the provider-specific parameters and requirements.

