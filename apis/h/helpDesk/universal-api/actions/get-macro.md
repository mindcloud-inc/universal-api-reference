# HelpDesk: Get Macro

Retrieves a macro from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-macro
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-macro?connectionId=$CONNECTION_ID&macroID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "macroID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-macro?${params}`, {
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
| `macroID` | string | yes | The HelpDesk macro ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "agentID": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByType": "string",
      "description": "string",
      "ID": "string",
      "licenseID": 1,
      "name": "Ava Chen",
      "teamIDs": [
        "string"
      ],
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
| `actions` | array<object> |  |
| `agentID` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdByType` | string |  |
| `description` | string |  |
| `ID` | string |  |
| `licenseID` | number |  |
| `name` | string |  |
| `teamIDs` | array<string> |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |

## Native endpoint

Through the native HelpDesk API, this operation is `GET /v1/macros/:macroID` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-macro.md) for the provider-specific parameters and requirements.

