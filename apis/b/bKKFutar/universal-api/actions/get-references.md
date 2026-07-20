# BKK Futar: Get References

Retrieves ID-based references from BKK Futar.

```
GET https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-references
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BKK Futar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-references?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-references?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agency_id` | string | no | Agency ID to resolve, such as BKK. |
| `alert_id` | string | no | Alert ID to resolve. |
| `route_id` | string | no | Route ID to resolve. |
| `stop_id` | string | no | Stop ID to resolve, such as BKK_F01227. |
| `include_references` | string | no | Reference data to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entry": {
        "errors": {
          "agencyIds": [
            "string"
          ],
          "alertIds": [
            "string"
          ],
          "routeIds": [
            "string"
          ],
          "stopIds": [
            "string"
          ]
        }
      },
      "limitExceeded": true,
      "references": {
        "agencies": {},
        "alerts": {},
        "routes": {},
        "stops": {},
        "trips": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entry.errors.agencyIds` | array<string> | Agency IDs that could not be resolved. |
| `entry.errors.alertIds` | array<string> | Alert IDs that could not be resolved. |
| `entry.errors.routeIds` | array<string> | Route IDs that could not be resolved. |
| `entry.errors.stopIds` | array<string> | Stop IDs that could not be resolved. |
| `limitExceeded` | boolean | Whether the response exceeded the defined limit. |
| `references` | object | Resolved agency, route, stop, trip, and alert references. |
| `references.agencies` | object |  |
| `references.alerts` | object |  |
| `references.routes` | object |  |
| `references.stops` | object |  |
| `references.trips` | object |  |

## Native endpoint

Through the native BKK Futar API, this operation is `GET /references.json` (base URL `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-references.md) for the provider-specific parameters and requirements.

