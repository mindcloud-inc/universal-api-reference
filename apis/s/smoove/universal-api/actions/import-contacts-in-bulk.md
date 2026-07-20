# Smoove: Import Contacts in Bulk

Imports contacts into Smoove in bulk.

```
POST https://connect.mindcloud.co/v1/universal/smoove/latest/actions/import-contacts-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/import-contacts-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smoove/latest/actions/import-contacts-in-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lists_ToSubscribe[]` | array<number> | no |  |
| `contacts[]` | array<object> | yes |  |
| `overrideNullableValue` | boolean | no | Default: `false`. |
| `updateOnlyExistingContacts` | boolean | no | Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "importReport": {
        "blacklisted": 1,
        "inserted": 1,
        "invalids": 1,
        "quotaExceeded": 1,
        "reportUrl": "https://example.com",
        "totalOperations": 1,
        "updated": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `importReport.blacklisted` | number |  |
| `importReport.inserted` | number |  |
| `importReport.invalids` | number |  |
| `importReport.quotaExceeded` | number |  |
| `importReport.reportUrl` | string |  |
| `importReport.totalOperations` | number |  |
| `importReport.updated` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Smoove API, this operation is `POST /v1/Contacts_BulkImport` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-contacts-in-bulk.md) for the provider-specific parameters and requirements.

