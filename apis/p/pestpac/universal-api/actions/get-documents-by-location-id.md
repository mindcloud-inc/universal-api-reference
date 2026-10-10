# PestPac: Get Documents by Location ID



```
GET https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/get-documents-by-location-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PestPac `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/get-documents-by-location-id?connectionId=$CONNECTION_ID&locationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/get-documents-by-location-id?${params}`, {
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
| `locationId` | number | yes | PestPac Location ID to list documents for. |

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

Through the native PestPac API, this operation is `GET Locations/:locationId/documents` (base URL `https://api.workwave.com/pestpac/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-documents-by-location-id.md) for the provider-specific parameters and requirements.

