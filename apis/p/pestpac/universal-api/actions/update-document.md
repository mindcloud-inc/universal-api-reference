# PestPac: Update Document



```
PUT https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PestPac `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": 1,
  "locationId": 1,
  "name": "Ava Chen",
  "date": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/update-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": 1,
    "locationId": 1,
    "name": "Ava Chen",
    "date": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | number | yes |  |
| `locationId` | number | yes |  |
| `name` | string | yes |  |
| `url` | string | no |  |
| `date` | date | yes |  |
| `tags` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ContentType": "string",
      "Date": "2026-05-07T12:00:00.000Z",
      "DocumentID": 1,
      "DocumentType": "string",
      "EndingEffectiveDate": "string",
      "FileName": "Ava Chen",
      "FileSize": 1,
      "FormData": "string",
      "IncludeOn": {},
      "IsTechPhoto": true,
      "Name": "Ava Chen",
      "OrderID": "string",
      "SetupID": "string",
      "StartingEffectiveDate": "string",
      "Tags": "string",
      "URL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ContentType` | string |  |
| `Date` | date |  |
| `DocumentID` | number |  |
| `DocumentType` | string |  |
| `EndingEffectiveDate` | string |  |
| `FileName` | string |  |
| `FileSize` | number |  |
| `FormData` | string |  |
| `IncludeOn` | object |  |
| `IsTechPhoto` | boolean |  |
| `Name` | string |  |
| `OrderID` | string |  |
| `SetupID` | string |  |
| `StartingEffectiveDate` | string |  |
| `Tags` | string |  |
| `URL` | string |  |

## Native endpoint

Through the native PestPac API, this operation is `PUT Documents/:documentId` (base URL `https://api.workwave.com/pestpac/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document.md) for the provider-specific parameters and requirements.

