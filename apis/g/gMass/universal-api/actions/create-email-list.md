# GMass: Create Email List

Creates an email list in GMass.

```
POST https://connect.mindcloud.co/v1/universal/gMass/latest/actions/create-email-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/create-email-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listSource.listSourceSheet.spreadsheetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gMass/latest/actions/create-email-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listSource.listSourceSheet.spreadsheetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listSource` | object | no |  |
| `listSource.listSourceSheet` | object | no |  |
| `listSource.listSourceSheet.spreadsheetId` | string | yes |  |
| `listSource.listSourceSheet.worksheetId` | string | no |  |
| `listSource.listSourceSheet.spreadsheetName` | string | no |  |
| `listSource.listSourceSheet.worksheetName` | string | no |  |
| `listSource.listSourceSheet.keepDuplicates` | boolean | no |  |
| `listSource.listSourceSheet.filterCriteria` | string | no |  |
| `listSource.listSourceSheet.andOr` | string | no |  |
| `listSource.listSourceSheet.updateSheet` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GMass API returns.

## Native endpoint

Through the native GMass API, this operation is `POST /lists` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-list.md) for the provider-specific parameters and requirements.

