# xMatters: Get an event

Retrieves an event from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-event?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-event?${params}`, {
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
| `eventId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotations": {
        "count": 1,
        "data": [
          {
            "author": {
              "firstName": "Ava",
              "id": "string",
              "lastName": "Chen",
              "links": {
                "self": "https://example.com"
              },
              "recipientType": "string",
              "targetName": "Ava Chen"
            },
            "comment": "string",
            "created": "2026-05-07T12:00:00.000Z",
            "event": {
              "eventId": "string",
              "id": "string",
              "links": {
                "self": "https://example.com"
              }
            },
            "id": "string"
          }
        ],
        "total": 1
      },
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
      "eventId": "string",
      "expirationInMinutes": 1,
      "floodControl": true,
      "form": {
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "incident": "string",
      "messages": {
        "count": 1,
        "data": [
          {
            "body": "string",
            "id": "string",
            "language": "string",
            "messageType": "string",
            "subject": "string"
          }
        ],
        "total": 1
      },
      "otherResponseCount": 1,
      "otherResponseCountThreshold": 1,
      "overrideDeviceRestrictions": true,
      "plan": {
        "id": "string",
        "name": "Ava Chen"
      },
      "priority": "string",
      "properties": {
        "myBooleanProperty": true,
        "myComboProperty": "string",
        "myHierarchyProperty": [
          {
            "category": "string",
            "value": "string"
          }
        ],
        "myListProperty": [
          [
            "string"
          ]
        ],
        "myNumberProperty": 1,
        "myPasswordProperty": "string",
        "myTextPropertyEn": "string"
      },
      "recipients": {
        "count": 1,
        "data": [
          {
            "allowDuplicates": true,
            "description": "string",
            "externallyOwned": true,
            "firstName": "Ava",
            "groupType": "string",
            "id": "string",
            "language": "string",
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "observedByAll": true,
            "phoneLogin": "string",
            "recipientType": "string",
            "responseCount": 1,
            "responseCountThreshold": 1,
            "site": {
              "id": "string",
              "links": {
                "self": "https://example.com"
              }
            },
            "status": "string",
            "targeted": true,
            "targetName": "Ava Chen",
            "timezone": "string",
            "useDefaultDevices": true,
            "webLogin": "string"
          }
        ],
        "links": {
          "self": "https://example.com"
        },
        "total": 1
      },
      "requirePhonePassword": true,
      "responseOptions": {
        "count": 1,
        "data": [
          {
            "action": "string",
            "allowComments": true,
            "contribution": "string",
            "description": "string",
            "id": "string",
            "joinConference": true,
            "number": 1,
            "prompt": "string",
            "text": "string"
          }
        ],
        "total": 1
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
      "terminated": "2026-05-07T12:00:00.000Z",
      "voicemailOptions": {
        "every": 1,
        "leave": "ava@example.com",
        "retry": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotations.count` | number |  |
| `annotations.data[].author.firstName` | string |  |
| `annotations.data[].author.id` | string |  |
| `annotations.data[].author.lastName` | string |  |
| `annotations.data[].author.links.self` | string |  |
| `annotations.data[].author.recipientType` | string |  |
| `annotations.data[].author.targetName` | string |  |
| `annotations.data[].comment` | string |  |
| `annotations.data[].created` | date |  |
| `annotations.data[].event.eventId` | string |  |
| `annotations.data[].event.id` | string |  |
| `annotations.data[].event.links.self` | string |  |
| `annotations.data[].id` | string |  |
| `annotations.total` | number |  |
| `bypassPhoneIntro` | boolean |  |
| `conference.bridgeId` | string |  |
| `conference.bridgeNumber` | string |  |
| `conference.id` | string |  |
| `conference.links.self` | string |  |
| `conference.type` | string |  |
| `created` | date |  |
| `eventId` | string |  |
| `expirationInMinutes` | number |  |
| `floodControl` | boolean |  |
| `form.id` | string |  |
| `form.name` | string |  |
| `id` | string |  |
| `incident` | string |  |
| `messages.count` | number |  |
| `messages.data[].body` | string |  |
| `messages.data[].id` | string |  |
| `messages.data[].language` | string |  |
| `messages.data[].messageType` | string |  |
| `messages.data[].subject` | string |  |
| `messages.total` | number |  |
| `otherResponseCount` | number |  |
| `otherResponseCountThreshold` | number |  |
| `overrideDeviceRestrictions` | boolean |  |
| `plan.id` | string |  |
| `plan.name` | string |  |
| `priority` | string |  |
| `properties.myBooleanProperty` | boolean |  |
| `properties.myComboProperty` | string |  |
| `properties.myHierarchyProperty[].category` | string |  |
| `properties.myHierarchyProperty[].value` | string |  |
| `properties.myListProperty[]` | array<string> |  |
| `properties.myNumberProperty` | number |  |
| `properties.myPasswordProperty` | string |  |
| `properties.myTextPropertyEn` | string |  |
| `recipients.count` | number |  |
| `recipients.data[].allowDuplicates` | boolean |  |
| `recipients.data[].description` | string |  |
| `recipients.data[].externallyOwned` | boolean |  |
| `recipients.data[].firstName` | string |  |
| `recipients.data[].groupType` | string |  |
| `recipients.data[].id` | string |  |
| `recipients.data[].language` | string |  |
| `recipients.data[].lastName` | string |  |
| `recipients.data[].links.self` | string |  |
| `recipients.data[].observedByAll` | boolean |  |
| `recipients.data[].phoneLogin` | string |  |
| `recipients.data[].recipientType` | string |  |
| `recipients.data[].responseCount` | number |  |
| `recipients.data[].responseCountThreshold` | number |  |
| `recipients.data[].site.id` | string |  |
| `recipients.data[].site.links.self` | string |  |
| `recipients.data[].status` | string |  |
| `recipients.data[].targeted` | boolean |  |
| `recipients.data[].targetName` | string |  |
| `recipients.data[].timezone` | string |  |
| `recipients.data[].useDefaultDevices` | boolean |  |
| `recipients.data[].webLogin` | string |  |
| `recipients.links.self` | string |  |
| `recipients.total` | number |  |
| `requirePhonePassword` | boolean |  |
| `responseOptions.count` | number |  |
| `responseOptions.data[].action` | string |  |
| `responseOptions.data[].allowComments` | boolean |  |
| `responseOptions.data[].contribution` | string |  |
| `responseOptions.data[].description` | string |  |
| `responseOptions.data[].id` | string |  |
| `responseOptions.data[].joinConference` | boolean |  |
| `responseOptions.data[].number` | number |  |
| `responseOptions.data[].prompt` | string |  |
| `responseOptions.data[].text` | string |  |
| `responseOptions.total` | number |  |
| `status` | string |  |
| `submitter.firstName` | string |  |
| `submitter.id` | string |  |
| `submitter.lastName` | string |  |
| `submitter.links.self` | string |  |
| `submitter.recipientType` | string |  |
| `submitter.targetName` | string |  |
| `terminated` | date |  |
| `voicemailOptions.every` | number |  |
| `voicemailOptions.leave` | string |  |
| `voicemailOptions.retry` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET events/{eventId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-an-event.md) for the provider-specific parameters and requirements.

