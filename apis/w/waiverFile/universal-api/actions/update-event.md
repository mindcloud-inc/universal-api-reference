# WaiverFile: Update Event

Updates an existing event in WaiverFile.

```
PUT https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventID": "string",
  "eventName": "Ava Chen",
  "dateStart": "2026-05-07T12:00:00.000Z",
  "dateEnd": "2026-05-07T12:00:00.000Z",
  "isAllDay": true,
  "eventCategoryID": "string",
  "waiverFormIDs[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventID": "string",
    "eventName": "Ava Chen",
    "dateStart": "2026-05-07T12:00:00.000Z",
    "dateEnd": "2026-05-07T12:00:00.000Z",
    "isAllDay": true,
    "eventCategoryID": "string",
    "waiverFormIDs[]": ["string"],
    "waiverFormIDs[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventID` | string | yes |  |
| `eventName` | string | yes |  |
| `dateStart` | date | yes |  |
| `dateEnd` | date | yes |  |
| `isAllDay` | boolean | yes |  |
| `eventCategoryID` | string | yes |  |
| `waiverFormIDs[]` | array | yes |  |
| `waiverFormIDs[]` | array | yes |  |

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

Through the native WaiverFile API, this operation is `POST /UpdateEvent` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

