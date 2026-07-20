# condoo: Create Pageview

Creates a new pageview in condoo.

```
POST https://connect.mindcloud.co/v1/universal/condoo/latest/actions/create-pageview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/create-pageview" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websiteId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/condoo/latest/actions/create-pageview', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "websiteId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `browserLanguage` | string | no | Optional browser language, such as en. |
| `browserName` | string | no | Optional browser name, such as Chrome. |
| `browserTimezone` | string | no | Optional browser timezone, such as UTC. |
| `cityName` | string | no | Optional city name. |
| `continentCode` | string | no | Optional continent code. Allowed values: AF, AN, AS, EU, NA, OC, SA. |
| `countryCode` | string | no | Optional ISO country code. |
| `deviceType` | string | no | Device type. Allowed values: desktop, mobile, tablet. |
| `osName` | string | no | Optional operating system name. |
| `path` | string | no | Optional page path when type is pageview. |
| `referrerHost` | string | no | Optional referrer host. |
| `referrerPath` | string | no | Optional referrer path, such as /page. |
| `screenResolution` | string | no | Optional screen resolution. |
| `theme` | string | no | Theme. Allowed values: light, dark. |
| `type` | string | no | Optional type. Allowed values: pageview, custom. Defaults to pageview. |
| `utmCampaign` | string | no | Optional UTM campaign. |
| `utmMedium` | string | no | Optional UTM medium. |
| `utmSource` | string | no | Optional UTM source. |
| `websiteId` | number | yes | Required website ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native condoo API, this operation is `POST /pageviews-lightweight` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pageview.md) for the provider-specific parameters and requirements.

