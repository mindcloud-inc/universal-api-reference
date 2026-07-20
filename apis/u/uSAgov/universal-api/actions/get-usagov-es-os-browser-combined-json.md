# USA.gov: List Spanish Site OS and Browser Combinations

Retrieves Spanish site OS and browser combinations from USA.gov.

```
GET https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-es-os-browser-combined-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USA.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-es-os-browser-combined-json?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-es-os-browser-combined-json?${params}`, {
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
| `meta.description` | string | Report description. |
| `meta.name` | string | Report display name. |
| `name` | string | Report file name. |
| `totals.activeUsers` | number | Total active users. |

## Native endpoint

Through the native USA.gov API, this operation is `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/os-browsers.json` (base URL `https://s3-us-gov-west-1.amazonaws.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usagov-es-os-browser-combined-json.md) for the provider-specific parameters and requirements.

