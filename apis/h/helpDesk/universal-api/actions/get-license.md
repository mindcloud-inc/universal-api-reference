# HelpDesk: Get License

Retrieves a license from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-license
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-license?connectionId=$CONNECTION_ID&licenseID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "licenseID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-license?${params}`, {
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
| `licenseID` | string | yes | Unique HelpDesk license ID. |

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

Through the native HelpDesk API, this operation is `GET /v1/licenses/:licenseID` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-license.md) for the provider-specific parameters and requirements.

