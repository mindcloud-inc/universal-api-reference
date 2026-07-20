# xMatters: Get form sections

Retrieves form sections from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-form-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-form-sections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-form-sections?${params}`, {
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
| `formId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "bypassPhoneIntro": {
            "orderNum": 1,
            "value": true,
            "visible": true
          },
          "collapsed": true,
          "enableResponseCounts": true,
          "escalationOverride": {
            "orderNum": 1,
            "value": true,
            "visible": true
          },
          "expandableGroups": true,
          "expiration": {
            "duration": 1,
            "orderNum": 1,
            "unit": "string",
            "visible": true
          },
          "expirationInMinutes": {
            "orderNum": 1,
            "value": 1,
            "visible": true
          },
          "form": {
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "visibility": "string"
          },
          "id": "string",
          "orderNum": 1,
          "overrideDeviceRestrictions": {
            "orderNum": 1,
            "value": true,
            "visible": true
          },
          "priority": {
            "orderNum": 1,
            "value": "string",
            "visible": true
          },
          "recipients": {
            "count": 1,
            "links": {
              "self": "https://example.com"
            },
            "total": 1
          },
          "requirePhonePassword": {
            "orderNum": 1,
            "value": true,
            "visible": true
          },
          "searchableTypes": {
            "devices": true,
            "groups": true,
            "services": true,
            "sites": true,
            "users": true
          },
          "title": "string",
          "type": "string",
          "visible": true,
          "voicemailOptions": {
            "every": 1,
            "leave": "ava@example.com",
            "leaveOptions": [
              {
                "name": "ava@example.com",
                "selected": true,
                "visible": true
              }
            ],
            "orderNum": 1,
            "retry": 1,
            "selected": true,
            "visible": true
          }
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
| `data[].bypassPhoneIntro.orderNum` | number |  |
| `data[].bypassPhoneIntro.value` | boolean |  |
| `data[].bypassPhoneIntro.visible` | boolean |  |
| `data[].collapsed` | boolean |  |
| `data[].enableResponseCounts` | boolean |  |
| `data[].escalationOverride.orderNum` | number |  |
| `data[].escalationOverride.value` | boolean |  |
| `data[].escalationOverride.visible` | boolean |  |
| `data[].expandableGroups` | boolean |  |
| `data[].expiration.duration` | number |  |
| `data[].expiration.orderNum` | number |  |
| `data[].expiration.unit` | string |  |
| `data[].expiration.visible` | boolean |  |
| `data[].expirationInMinutes.orderNum` | number |  |
| `data[].expirationInMinutes.value` | number |  |
| `data[].expirationInMinutes.visible` | boolean |  |
| `data[].form.id` | string |  |
| `data[].form.links.self` | string |  |
| `data[].form.visibility` | string |  |
| `data[].id` | string |  |
| `data[].orderNum` | number |  |
| `data[].overrideDeviceRestrictions.orderNum` | number |  |
| `data[].overrideDeviceRestrictions.value` | boolean |  |
| `data[].overrideDeviceRestrictions.visible` | boolean |  |
| `data[].priority.orderNum` | number |  |
| `data[].priority.value` | string |  |
| `data[].priority.visible` | boolean |  |
| `data[].recipients.count` | number |  |
| `data[].recipients.links.self` | string |  |
| `data[].recipients.total` | number |  |
| `data[].requirePhonePassword.orderNum` | number |  |
| `data[].requirePhonePassword.value` | boolean |  |
| `data[].requirePhonePassword.visible` | boolean |  |
| `data[].searchableTypes.devices` | boolean |  |
| `data[].searchableTypes.groups` | boolean |  |
| `data[].searchableTypes.services` | boolean |  |
| `data[].searchableTypes.sites` | boolean |  |
| `data[].searchableTypes.users` | boolean |  |
| `data[].title` | string |  |
| `data[].type` | string |  |
| `data[].visible` | boolean |  |
| `data[].voicemailOptions.every` | number |  |
| `data[].voicemailOptions.leave` | string |  |
| `data[].voicemailOptions.leaveOptions[].name` | string |  |
| `data[].voicemailOptions.leaveOptions[].selected` | boolean |  |
| `data[].voicemailOptions.leaveOptions[].visible` | boolean |  |
| `data[].voicemailOptions.orderNum` | number |  |
| `data[].voicemailOptions.retry` | number |  |
| `data[].voicemailOptions.selected` | boolean |  |
| `data[].voicemailOptions.visible` | boolean |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET forms/{formId}/sections` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-form-sections.md) for the provider-specific parameters and requirements.

