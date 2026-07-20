# HelpDesk: Get Tag

Retrieves a tag from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-tag?connectionId=$CONNECTION_ID&tagID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/get-tag?${params}`, {
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
| `tagID` | string | yes | Unique HelpDesk tag ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByType": "string",
      "ID": "string",
      "licenseID": 1,
      "name": "Ava Chen",
      "teamID": "string",
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
| `count` | number |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdByType` | string |  |
| `ID` | string |  |
| `licenseID` | number |  |
| `name` | string |  |
| `teamID` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |

## Native endpoint

Through the native HelpDesk API, this operation is `GET /v1/tags/:tagID` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.

