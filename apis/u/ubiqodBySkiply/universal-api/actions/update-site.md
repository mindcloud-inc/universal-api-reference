# Ubiqod by Skiply: Update Site



```
PUT https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/update-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubiqod by Skiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/update-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/update-site', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | yes | Site ID. |
| `label` | string | no | Updated site label. |
| `coordinates` | object | no | Updated site coordinates object with latitude and longitude. |
| `distanceMargin` | number | no | Updated geofencing distance margin in meters. Ubiqod requires at least 50 when provided. |
| `externalReferences` | object | no | Updated external reference map for the site. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "distanceMargin": 1,
      "externalReferences": {},
      "id": "string",
      "label": "string",
      "latitude": 1,
      "longitude": 1,
      "state": "string",
      "street": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | City. |
| `country` | string | Country. |
| `distanceMargin` | number | Distance margin in meters. |
| `externalReferences` | object | External reference map. |
| `id` | string | Site ID. |
| `label` | string | Site label. |
| `latitude` | number | Site latitude. |
| `longitude` | number | Site longitude. |
| `state` | string | State or region. |
| `street` | string | Street. |
| `zipCode` | string | ZIP or postal code. |

## Native endpoint

Through the native Ubiqod by Skiply API, this operation is `PATCH /sites/:siteId` (base URL `https://api.ubiqod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-site.md) for the provider-specific parameters and requirements.

