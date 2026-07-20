# condoo: Update Website

Updates an existing website in condoo.

```
PUT https://connect.mindcloud.co/v1/universal/condoo/latest/actions/update-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/update-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websiteId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/condoo/latest/actions/update-website', {
  method: 'PUT',
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
| `botExclusionIsEnabled` | boolean | no | Whether bot exclusion is enabled. |
| `domainId` | number | no | Optional domain ID to associate with the website. |
| `emailReportsIsEnabled` | boolean | no | Whether email reports are enabled. |
| `eventsChildrenIsEnabled` | boolean | no | Whether child event tracking is enabled. |
| `excludedIps` | string | no | Optional excluded IP list. |
| `host` | string | no | Optional website host. |
| `isEnabled` | boolean | no | Optional enabled toggle. |
| `name` | string | no | Optional website name. |
| `outboundClicksIsEnabled` | boolean | no | Optional outbound-click tracking toggle. |
| `publicStatisticsIsEnabled` | boolean | no | Optional public statistics toggle. |
| `publicStatisticsPassword` | string | no | Optional password when public statistics are enabled. |
| `queryParametersTrackingIsEnabled` | boolean | no | Whether query parameter tracking is enabled. |
| `scheme` | string | no | Optional URL scheme. Allowed values: http, https. |
| `sessionsReplaysHideTextSelector` | string | no | Optional selector for text hidden in session replays. |
| `sessionsReplaysIsEnabled` | boolean | no | Whether session replays are enabled. |
| `trackingType` | string | no | Optional tracking type. Allowed values: normal, lightweight. |
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

Through the native condoo API, this operation is `POST /websites/{website_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-website.md) for the provider-specific parameters and requirements.

