# HelpDesk: List Rules

Retrieves rules from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-rules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-rules?${params}`, {
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
      "actions": [
        {}
      ],
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByType": "string",
      "description": "string",
      "ID": "string",
      "licenseID": 1,
      "limitPerTicket": 1,
      "name": "Ava Chen",
      "ordering": 1,
      "quantifier": "string",
      "triggers": [
        {}
      ],
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "useCounter": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> |  |
| `active` | boolean |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdByType` | string |  |
| `description` | string |  |
| `ID` | string |  |
| `licenseID` | number |  |
| `limitPerTicket` | number |  |
| `name` | string |  |
| `ordering` | number |  |
| `quantifier` | string |  |
| `triggers` | array<object> |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `useCounter` | number |  |

## Native endpoint

Through the native HelpDesk API, this operation is `GET /v1/rules` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rules.md) for the provider-specific parameters and requirements.

