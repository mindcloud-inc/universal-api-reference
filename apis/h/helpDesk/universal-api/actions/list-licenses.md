# HelpDesk: List Licenses

Retrieves licenses from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-licenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-licenses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-licenses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "availableSources": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "defaultTeamID": "string",
      "defaultTemplateID": "string",
      "detectedLanguages": [
        "string"
      ],
      "flags": {},
      "ID": 1,
      "settings": {
        "companyName": "Ava Chen",
        "externalTickets": true,
        "poweredByFooter": true,
        "ticketThread": true
      },
      "source": {
        "landingPage": "string",
        "referrer": "string",
        "utmMedium": "string",
        "utmSource": "string"
      },
      "subscription": {
        "pastDue": true,
        "state": "string"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "verifiedAt": "2026-05-07T12:00:00.000Z",
      "verifiedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableSources` | array<string> |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `defaultTeamID` | string |  |
| `defaultTemplateID` | string |  |
| `detectedLanguages` | array<string> |  |
| `flags` | object |  |
| `ID` | number |  |
| `settings` | object |  |
| `settings.companyName` | string |  |
| `settings.externalTickets` | boolean |  |
| `settings.poweredByFooter` | boolean |  |
| `settings.ticketThread` | boolean |  |
| `source` | object |  |
| `source.landingPage` | string |  |
| `source.referrer` | string |  |
| `source.utmMedium` | string |  |
| `source.utmSource` | string |  |
| `subscription` | object |  |
| `subscription.pastDue` | boolean |  |
| `subscription.state` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `verifiedAt` | date |  |
| `verifiedBy` | string |  |

## Native endpoint

Through the native HelpDesk API, this operation is `GET /v1/licenses` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-licenses.md) for the provider-specific parameters and requirements.

