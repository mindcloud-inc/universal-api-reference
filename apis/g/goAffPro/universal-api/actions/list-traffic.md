# GoAffPro: List Traffic

Retrieves affiliate traffic data from GoAffPro.

```
GET https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-traffic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-traffic?connectionId=$CONNECTION_ID&fields%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fields[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-traffic?${params}`, {
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
| `affiliateId` | string | no | Only return traffic for this affiliate ID. |
| `fields[]` | array<string> | yes | Fields to include in returned traffic records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "ipAddress": "string",
      "landingPage": "string",
      "referringPage": "string",
      "userAgent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | number |  |
| `createdAt` | date |  |
| `id` | number |  |
| `ipAddress` | string |  |
| `landingPage` | string |  |
| `referringPage` | string |  |
| `userAgent` | string |  |

## Native endpoint

Through the native GoAffPro API, this operation is `GET /admin/traffic` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-traffic.md) for the provider-specific parameters and requirements.

