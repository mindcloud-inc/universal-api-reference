# Routee: Get paged analytics

Retrieves paged analytics data from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-paged-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-paged-analytics?connectionId=$CONNECTION_ID&trackingId=string&from=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingId": "string",
  "from": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-paged-analytics?${params}`, {
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
| `trackingId` | string | yes |  |
| `from` | string | yes | Start date for analytics report |
| `to` | string | yes | End date for analytics report |
| `page` | string | no | [Optional] Index for results (0 is first result) |
| `size` | string | no | [Optional] Number of results per page (Default 20 max according to capability) |
| `link` | string | no | The shortened URL |
| `longUrl` | string | no | The original URL |
| `visits[]` | array<object> | no | The information for each click on the shortened URL. |
| `tags` | string | no | A map of string field values to store information |

## Response

```json
{
  "success": true,
  "data": [
    {
      "link": "https://example.com",
      "longUrl": "https://example.com",
      "tags": {
        "tag1": "string",
        "tag2": "string"
      },
      "visits": {
        "content": [
          [
            "string"
          ]
        ],
        "first": true,
        "last": true,
        "number": 1,
        "numberOfElements": 1,
        "size": 1,
        "totalElements": 1,
        "totalPages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | string |  |
| `longUrl` | string |  |
| `tags` | object |  |
| `tags.tag1` | string |  |
| `tags.tag2` | string |  |
| `visits` | object |  |
| `visits.content[]` | array |  |
| `visits.first` | boolean |  |
| `visits.last` | boolean |  |
| `visits.number` | number |  |
| `visits.numberOfElements` | number |  |
| `visits.size` | number |  |
| `visits.totalElements` | number |  |
| `visits.totalPages` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /shorten/:trackingId/analytics` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-paged-analytics.md) for the provider-specific parameters and requirements.

