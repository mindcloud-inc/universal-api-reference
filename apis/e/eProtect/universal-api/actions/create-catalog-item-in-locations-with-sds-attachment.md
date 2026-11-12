# 3E Protect: Create Catalog Item in Locations with SDS Attachment



```
POST https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/create-catalog-item-in-locations-with-sds-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/create-catalog-item-in-locations-with-sds-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "manufacturerName": "Ava Chen",
  "materialName": "Ava Chen",
  "source": "string",
  "identifier": "string",
  "locationNames[]": [
    "Ava Chen"
  ],
  "fileBytes": "string",
  "fileName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/create-catalog-item-in-locations-with-sds-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "manufacturerName": "Ava Chen",
    "materialName": "Ava Chen",
    "source": "string",
    "identifier": "string",
    "locationNames[]": ["Ava Chen"],
    "fileBytes": "string",
    "fileName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `manufacturerName` | string | yes |  |
| `materialName` | string | yes |  |
| `source` | string | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | string | yes | Your product identifier value for the selected source. |
| `locationNames[]` | array<string> | yes | Existing 3E location names. Retrieve them with List Locations. |
| `fileBytes` | string | yes | PDF contents encoded as Base64, a text representation of file bytes. |
| `fileName` | string | yes | PDF file name, including the .pdf extension. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productNumber` | string | no |  |
| `customValues[]` | array<object> | no | Customer-defined product fields, each supplied as a name and value. |
| `customValues[].name` | string | no |  |
| `customValues[].value` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3E Protect API returns.

## Native endpoint

Through the native 3E Protect API, this operation is `POST /catalog-item-location-attachment` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-catalog-item-in-locations-with-sds-attachment.md) for the provider-specific parameters and requirements.

