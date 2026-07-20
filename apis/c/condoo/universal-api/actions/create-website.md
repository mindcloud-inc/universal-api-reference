# condoo: Create Website

Creates a new website in condoo.

```
POST https://connect.mindcloud.co/v1/universal/condoo/latest/actions/create-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/create-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "host": "string",
  "name": "Ava Chen",
  "scheme": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/condoo/latest/actions/create-website', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "host": "string",
    "name": "Ava Chen",
    "scheme": "string"
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
| `host` | string | yes | Required website host. |
| `isEnabled` | boolean | no | Optional enabled toggle. |
| `name` | string | yes | Required website name. |
| `outboundClicksIsEnabled` | boolean | no | Optional outbound-click tracking toggle. |
| `publicStatisticsIsEnabled` | boolean | no | Optional public statistics toggle. |
| `publicStatisticsPassword` | string | no | Optional password when public statistics are enabled. |
| `queryParametersTrackingIsEnabled` | boolean | no | Whether query parameter tracking is enabled. |
| `scheme` | string | yes | Required URL scheme. Allowed values: http, https. |
| `sessionsReplaysHideTextSelector` | string | no | Optional selector for text hidden in session replays. |
| `sessionsReplaysIsEnabled` | boolean | no | Whether session replays are enabled. |
| `trackingType` | string | no | Optional tracking type. Allowed values: normal, lightweight. |

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

Through the native condoo API, this operation is `POST /websites` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-website.md) for the provider-specific parameters and requirements.

