# xMatters: Create a scenario

Creates a scenario in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-scenario
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-scenario" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-scenario', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachments` | list<string> | no |  |
| `bypassPhoneIntro` | boolean | no |  |
| `description` | string | no |  |
| `escalationOverride` | boolean | no |  |
| `expirationInMinutes` | number | no |  |
| `formId` | string | no |  |
| `name` | string | no |  |
| `overrideDeviceRestrictions` | boolean | no |  |
| `permitted` | list<string> | no |  |
| `priority` | string | no |  |
| `properties` | string | no |  |
| `recipients` | list<string> | no |  |
| `requirePhonePassword` | boolean | no |  |
| `senderOverrides` | string | no |  |
| `targetDeviceNames` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": {
        "count": 1,
        "data": {
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen",
          "path": "string",
          "size": 1
        },
        "total": 1
      },
      "bypassPhoneIntro": true,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "escalationOverride": true,
      "expirationInMinutes": 1,
      "form": {
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "overrideDeviceRestrictions": true,
      "permitted": {
        "count": 1,
        "data": [
          {
            "displayName": "Ava Chen",
            "hasEditPermission": true,
            "permissionType": "string",
            "person": {
              "firstName": "Ava",
              "id": "string",
              "lastName": "Chen",
              "links": {
                "self": "https://example.com"
              },
              "recipientType": "string",
              "targetName": "Ava Chen"
            },
            "recipientId": "string"
          }
        ],
        "total": 1
      },
      "plan": {
        "id": "string",
        "name": "Ava Chen"
      },
      "position": 1,
      "priority": "string",
      "properties": {
        "assignment": [
          {
            "category": "string",
            "value": "string"
          }
        ],
        "startTime": "2026-05-07T12:00:00.000Z",
        "summary": "string"
      },
      "recipients": {
        "count": 1,
        "data": [
          {
            "allowDuplicates": true,
            "description": "string",
            "externallyOwned": true,
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "observedByAll": true,
            "recipientType": "string",
            "status": "string",
            "targeted": true,
            "targetName": "Ava Chen",
            "useDefaultDevices": true
          }
        ],
        "total": 1
      },
      "requirePhonePassword": true,
      "senderOverrides": {
        "callerId": "string",
        "displayName": "Ava Chen"
      },
      "targetDeviceNames": {
        "count": 1,
        "data": [
          {
            "deviceType": "Ava Chen",
            "name": "Ava Chen"
          }
        ],
        "total": 1
      },
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
| `attachments.count` | number |  |
| `attachments.data.links.self` | string |  |
| `attachments.data.name` | string |  |
| `attachments.data.path` | string |  |
| `attachments.data.size` | number |  |
| `attachments.total` | number |  |
| `bypassPhoneIntro` | boolean |  |
| `created` | date |  |
| `description` | string |  |
| `escalationOverride` | boolean |  |
| `expirationInMinutes` | number |  |
| `form.id` | string |  |
| `form.name` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `name` | string |  |
| `overrideDeviceRestrictions` | boolean |  |
| `permitted.count` | number |  |
| `permitted.data[].displayName` | string |  |
| `permitted.data[].hasEditPermission` | boolean |  |
| `permitted.data[].permissionType` | string |  |
| `permitted.data[].person.firstName` | string |  |
| `permitted.data[].person.id` | string |  |
| `permitted.data[].person.lastName` | string |  |
| `permitted.data[].person.links.self` | string |  |
| `permitted.data[].person.recipientType` | string |  |
| `permitted.data[].person.targetName` | string |  |
| `permitted.data[].recipientId` | string |  |
| `permitted.total` | number |  |
| `plan.id` | string |  |
| `plan.name` | string |  |
| `position` | number |  |
| `priority` | string |  |
| `properties.assignment[].category` | string |  |
| `properties.assignment[].value` | string |  |
| `properties.startTime` | date |  |
| `properties.summary` | string |  |
| `recipients.count` | number |  |
| `recipients.data[].allowDuplicates` | boolean |  |
| `recipients.data[].description` | string |  |
| `recipients.data[].externallyOwned` | boolean |  |
| `recipients.data[].id` | string |  |
| `recipients.data[].links.self` | string |  |
| `recipients.data[].observedByAll` | boolean |  |
| `recipients.data[].recipientType` | string |  |
| `recipients.data[].status` | string |  |
| `recipients.data[].targeted` | boolean |  |
| `recipients.data[].targetName` | string |  |
| `recipients.data[].useDefaultDevices` | boolean |  |
| `recipients.total` | number |  |
| `requirePhonePassword` | boolean |  |
| `senderOverrides.callerId` | string |  |
| `senderOverrides.displayName` | string |  |
| `targetDeviceNames.count` | number |  |
| `targetDeviceNames.data[].deviceType` | string |  |
| `targetDeviceNames.data[].name` | string |  |
| `targetDeviceNames.total` | number |  |
| `voicemailOptions.every` | number |  |
| `voicemailOptions.leave` | string |  |
| `voicemailOptions.retry` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `POST forms/{formId}/scenarios` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-scenario.md) for the provider-specific parameters and requirements.

