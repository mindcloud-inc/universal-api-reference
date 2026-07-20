# xMatters: Get events

Retrieves events from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-events?${params}`, {
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
| `embed` | string | no |  |
| `priority` | string | no |  |
| `propertyName` | string | no |  |
| `propertyValue` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "bypassPhoneIntro": true,
          "conference": {
            "bridgeId": "string",
            "bridgeNumber": "string",
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "type": "string"
          },
          "created": "2026-05-07T12:00:00.000Z",
          "escalationOverride": true,
          "eventId": "string",
          "eventType": "string",
          "floodControl": true,
          "form": {
            "id": "string",
            "name": "Ava Chen"
          },
          "id": "string",
          "incident": "string",
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen",
          "otherResponseCount": 1,
          "otherResponseCountThreshold": 1,
          "overrideDeviceRestrictions": true,
          "plan": {
            "id": "string",
            "name": "Ava Chen"
          },
          "priority": "string",
          "properties": {
            "countryEn": "string",
            "customerReported": true,
            "customersAffected": 1
          },
          "requirePhonePassword": true,
          "responseCountsEnabled": true,
          "revision": {
            "at": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "seq": "string"
          },
          "status": "string",
          "submitter": {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "terminated": "2026-05-07T12:00:00.000Z"
        }
      ],
      "links": {
        "self": "https://example.com"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].bypassPhoneIntro` | boolean |  |
| `data[].conference.bridgeId` | string |  |
| `data[].conference.bridgeNumber` | string |  |
| `data[].conference.id` | string |  |
| `data[].conference.links.self` | string |  |
| `data[].conference.type` | string |  |
| `data[].created` | date |  |
| `data[].escalationOverride` | boolean |  |
| `data[].eventId` | string |  |
| `data[].eventType` | string |  |
| `data[].floodControl` | boolean |  |
| `data[].form.id` | string |  |
| `data[].form.name` | string |  |
| `data[].id` | string |  |
| `data[].incident` | string |  |
| `data[].links.self` | string |  |
| `data[].name` | string |  |
| `data[].otherResponseCount` | number |  |
| `data[].otherResponseCountThreshold` | number |  |
| `data[].overrideDeviceRestrictions` | boolean |  |
| `data[].plan.id` | string |  |
| `data[].plan.name` | string |  |
| `data[].priority` | string |  |
| `data[].properties.countryEn` | string |  |
| `data[].properties.customerReported` | boolean |  |
| `data[].properties.customersAffected` | number |  |
| `data[].requirePhonePassword` | boolean |  |
| `data[].responseCountsEnabled` | boolean |  |
| `data[].revision.at` | date |  |
| `data[].revision.id` | string |  |
| `data[].revision.seq` | string |  |
| `data[].status` | string |  |
| `data[].submitter.firstName` | string |  |
| `data[].submitter.id` | string |  |
| `data[].submitter.lastName` | string |  |
| `data[].submitter.links.self` | string |  |
| `data[].submitter.recipientType` | string |  |
| `data[].submitter.targetName` | string |  |
| `data[].terminated` | date |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET events` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-events.md) for the provider-specific parameters and requirements.

