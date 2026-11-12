# 3E Protect: Create Catalog Item with SDS Attachment



```
POST https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/create-catalog-item-with-sds-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/create-catalog-item-with-sds-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileBytes": "string",
  "fileName": "Ava Chen",
  "manufacturerName": "Ava Chen",
  "materialName": "Ava Chen",
  "obtainmentTypes[]": [
    {}
  ],
  "source": "string",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/create-catalog-item-with-sds-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileBytes": "string",
    "fileName": "Ava Chen",
    "manufacturerName": "Ava Chen",
    "materialName": "Ava Chen",
    "obtainmentTypes[]": [{}],
    "source": "string",
    "identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileBytes` | string | yes | PDF contents encoded as Base64, a text representation of file bytes. |
| `fileName` | string | yes | PDF file name, including the .pdf extension. |
| `manufacturerName` | string | yes |  |
| `materialName` | string | yes |  |
| `obtainmentTypes[]` | array<object> | yes | SDS obtainment (sourcing) targets, each defined by a language and country. |
| `source` | string | yes | Exact, case-sensitive product identifier source name agreed with 3E. |
| `identifier` | string | yes | Your product identifier value for the selected source. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `obtainmentTypes[].locale` | string | no | Two-letter language code, such as en. Use a language configured in List SDS Requirements. Example: `en`. |
| `obtainmentTypes[].country` | string | no | Three-letter country code, such as USA. Use a country configured in List SDS Requirements. Example: `USA`. |
| `productNumber` | string | no |  |
| `customValues[]` | array<object> | no | Customer-defined product fields, each supplied as a name and value. |
| `customValues[].name` | string | no |  |
| `customValues[].value` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3E Protect API returns.

## Native endpoint

Through the native 3E Protect API, this operation is `POST /catalog-item-attachment` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-catalog-item-with-sds-attachment.md) for the provider-specific parameters and requirements.

