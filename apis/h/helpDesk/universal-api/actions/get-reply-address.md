# HelpDesk: Get Reply Address

Retrieves a reply address from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-reply-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-reply-address?connectionId=$CONNECTION_ID&replyAddressID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "replyAddressID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-reply-address?${params}`, {
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
| `replyAddressID` | string | yes | The HelpDesk reply address ID. |

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
      "emailDomainID": "ava@example.com",
      "ID": "string",
      "licenseID": 1,
      "prefix": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "verified": true
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
| `emailDomainID` | string |  |
| `ID` | string |  |
| `licenseID` | number |  |
| `prefix` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native HelpDesk API, this operation is `GET /v1/replyAddresses/:replyAddressID` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reply-address.md) for the provider-specific parameters and requirements.

