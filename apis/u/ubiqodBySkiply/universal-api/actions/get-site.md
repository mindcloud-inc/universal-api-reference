# Ubiqod by Skiply: Get Site



```
GET https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubiqod by Skiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/get-site?connectionId=$CONNECTION_ID&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/get-site?${params}`, {
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
| `siteId` | string | yes | Site ID. |

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

Through the native Ubiqod by Skiply API, this operation is `GET /sites/:siteId` (base URL `https://api.ubiqod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

