# HelpDesk: Get Trusted Email

Retrieves a trusted email from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-trusted-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-trusted-email?connectionId=$CONNECTION_ID&trustedEmailID=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trustedEmailID": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-trusted-email?${params}`, {
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
| `trustedEmailID` | string | yes | The HelpDesk trusted email ID. |

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

Through the native HelpDesk API, this operation is `GET /v1/trustedEmails/:trustedEmailID` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trusted-email.md) for the provider-specific parameters and requirements.

