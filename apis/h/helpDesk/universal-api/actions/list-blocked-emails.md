# HelpDesk: List Blocked Emails

Retrieves blocked emails from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-blocked-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-blocked-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-blocked-emails?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByType": "string",
      "email": "ava@example.com",
      "ID": "string",
      "licenseID": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdByType` | string |  |
| `email` | string |  |
| `ID` | string |  |
| `licenseID` | number |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |

## Native endpoint

Through the native HelpDesk API, this operation is `GET /v1/blockedEmails` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blocked-emails.md) for the provider-specific parameters and requirements.

