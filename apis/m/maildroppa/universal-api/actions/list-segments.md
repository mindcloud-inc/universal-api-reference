# Maildroppa: List Segments



```
GET https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/list-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/list-segments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/list-segments?${params}`, {
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
      "expression": {
        "filterGroups": [
          {
            "elements": [
              {}
            ]
          }
        ],
        "operator": "string"
      },
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expression.filterGroups[].elements` | array<object> | List of filter elements in this group. |
| `expression.operator` | string | Logical operator that applies between filter groups. |
| `id` | string | Unique identifier of the segment. |
| `name` | string | Display name for the segment. |

## Native endpoint

Through the native Maildroppa API, this operation is `GET /subscriber/segment` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segments.md) for the provider-specific parameters and requirements.

