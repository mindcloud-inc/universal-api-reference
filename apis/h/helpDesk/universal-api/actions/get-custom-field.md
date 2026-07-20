# HelpDesk: Get Custom Field

Retrieves a custom field from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-custom-field?connectionId=$CONNECTION_ID&customFieldID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customFieldID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-custom-field?${params}`, {
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
| `customFieldID` | string | yes | The HelpDesk custom field ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKey": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByType": "string",
      "displayName": "Ava Chen",
      "ID": "string",
      "licenseID": 1,
      "roleLevel": "string",
      "status": "string",
      "teamIDs": [
        "string"
      ],
      "type": "string",
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
| `apiKey` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdByType` | string |  |
| `displayName` | string |  |
| `ID` | string |  |
| `licenseID` | number |  |
| `roleLevel` | string |  |
| `status` | string |  |
| `teamIDs` | array<string> |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |

## Native endpoint

Through the native HelpDesk API, this operation is `GET /v1/customFields/:customFieldID` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-field.md) for the provider-specific parameters and requirements.

