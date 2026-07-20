# Extract Monster: Extract Data From Text

Extracts structured data from text in Extract Monster.

```
GET https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/extract-data-from-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extract Monster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/extract-data-from-text?connectionId=$CONNECTION_ID&text=Enter%20the%20text%20to%20extract%20structured%20data%20from." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Enter the text to extract structured data from."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extractMonster/latest/actions/extract-data-from-text?${params}`, {
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
| `text` | string | yes | Text content to analyze and extract data from. Example: `Enter the text to extract structured data from.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schemaJson` | string | no | Optional JSON schema string used to structure the extraction result. Example: `Optional JSON schema string.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extractedData": {},
      "status": "string",
      "textLength": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extractedData` | object | Structured extraction payload returned for the text input. |
| `status` | string | Extraction request status. |
| `textLength` | number | Length of the analyzed text input. |

## Native endpoint

Through the native Extract Monster API, this operation is `POST /v1/extract/text` (base URL `https://api.extract.monster`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data-from-text.md) for the provider-specific parameters and requirements.

