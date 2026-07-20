# USA.gov: List Spanish Site Top Exit Pages

Retrieves Spanish site top exit pages from USA.gov.

```
GET https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-es-top-exit-pages-30-days-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USA.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-es-top-exit-pages-30-days-json?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-es-top-exit-pages-30-days-json?${params}`, {
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
      "data": [
        [
          {}
        ]
      ],
      "meta": {
        "description": "string",
        "name": "Ava Chen"
      },
      "name": "Ava Chen",
      "totals": {
        "users": 1,
        "visits": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> | Report rows. |
| `data[].exits` | string | Exit count for the exit page row. |
| `data[].pageviews` | string | Page view count for the exit page row. |
| `data[].users` | string | User count for the exit page row. |
| `data[].visits` | string | Visit count for the exit page row. |
| `meta.description` | string | Report description. |
| `meta.name` | string | Report display name. |
| `name` | string | Report file name. |
| `totals.users` | number | Total users. |
| `totals.visits` | number | Total visits. |

## Native endpoint

Through the native USA.gov API, this operation is `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/top-exit-pages-30-days.json` (base URL `https://s3-us-gov-west-1.amazonaws.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usagov-es-top-exit-pages-30-days-json.md) for the provider-specific parameters and requirements.

