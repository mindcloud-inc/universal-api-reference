# HelpDesk: List Canned Responses

Retrieves canned responses from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-canned-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-canned-responses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-canned-responses?${params}`, {
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
      "attachments": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByType": "string",
      "ID": "string",
      "licenseID": 1,
      "richTextObj": {},
      "shortcuts": [
        "string"
      ],
      "teamID": "string",
      "text": "string",
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
| `attachments` | array<object> |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdByType` | string |  |
| `ID` | string |  |
| `licenseID` | number |  |
| `richTextObj` | object |  |
| `shortcuts` | array<string> |  |
| `teamID` | string |  |
| `text` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |

## Native endpoint

Through the native HelpDesk API, this operation is `GET /v1/cannedResponses` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-canned-responses.md) for the provider-specific parameters and requirements.

