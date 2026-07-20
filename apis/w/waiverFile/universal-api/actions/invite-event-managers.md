# WaiverFile: Invite Event Managers

Invites event managers to an event in WaiverFile.

```
POST https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/invite-event-managers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/invite-event-managers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventID": "string",
  "emailAddresses": "ava@example.com",
  "managerEmailMessage": "ava@example.com",
  "skipSendingEmailIfAccountExists": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/invite-event-managers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventID": "string",
    "emailAddresses": "ava@example.com",
    "managerEmailMessage": "ava@example.com",
    "skipSendingEmailIfAccountExists": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventID` | string | yes |  |
| `emailAddresses` | string | yes |  |
| `managerEmailMessage` | string | yes |  |
| `skipSendingEmailIfAccountExists` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_waiverForms": [
        {}
      ],
      "_waivers": [
        {}
      ],
      "_WPObjectStatus": 1,
      "<Category>k__BackingField": {},
      "me": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_waiverForms` | array<object> |  |
| `_waivers` | array<object> |  |
| `_WPObjectStatus` | number |  |
| `<Category>k__BackingField` | object |  |
| `me` | object |  |

## Native endpoint

Through the native WaiverFile API, this operation is `POST /InviteEventManagers` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-event-managers.md) for the provider-specific parameters and requirements.

