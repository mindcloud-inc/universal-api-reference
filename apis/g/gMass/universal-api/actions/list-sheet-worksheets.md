# GMass: List Sheet Worksheets

Retrieves worksheets from a connected Google Sheet in GMass.

```
GET https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-sheet-worksheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-sheet-worksheets?connectionId=$CONNECTION_ID&sheetid=1A2B3C4D5E" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sheetid": "1A2B3C4D5E"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-sheet-worksheets?${params}`, {
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
| `sheetid` | string | yes | Google Sheet ID to list worksheets for. Example: `1A2B3C4D5E`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "worksheetId": 1,
      "worksheetName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `worksheetId` | number | Google-assigned worksheet ID. |
| `worksheetName` | string | Worksheet tab name. |

## Native endpoint

Through the native GMass API, this operation is `GET /sheets/:sheetid/worksheets` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sheet-worksheets.md) for the provider-specific parameters and requirements.

