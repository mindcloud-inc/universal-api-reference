# Tidio: List Contact Properties [Plus plan]

Retrieves custom contact properties from Tidio.

```
GET https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-contact-properties-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-contact-properties-plus-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-contact-properties-plus-plan?${params}`, {
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
      "meta": {
        "cursor": "string",
        "limit": 1
      },
      "properties": [
        {
          "label": "string",
          "name": "Ava Chen",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object |  |
| `meta.cursor` | string | Value to fetch the next page. Null means the page is the last one. |
| `meta.limit` | number | How many items were displayed on list |
| `properties` | array<object> |  |
| `properties[]` | object |  |
| `properties[].label` | string | Label of contact property |
| `properties[].name` | string | It is described 'Internal property name' in tidio.com panel. It is treated as property id. |
| `properties[].type` | string | Type of contact property |

## Native endpoint

Through the native Tidio API, this operation is `GET /contact-properties` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-properties-plus-plan.md) for the provider-specific parameters and requirements.

