# USA.gov: List English Site Visitors by City

Retrieves English site visitors by city from USA.gov.

```
GET https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-visitors-per-city-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USA.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-visitors-per-city-json?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-visitors-per-city-json?${params}`, {
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
        "activeUsers": 1
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
| `data[].activeUsers` | string | Active users for the city row. |
| `data[].city` | string | Visitor city. |
| `meta.description` | string | Report description. |
| `meta.name` | string | Report display name. |
| `name` | string | Report file name. |
| `totals.activeUsers` | number | Total active users. |

## Native endpoint

Through the native USA.gov API, this operation is `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/top-cities-90-days.json` (base URL `https://s3-us-gov-west-1.amazonaws.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usagov-visitors-per-city-json.md) for the provider-specific parameters and requirements.

