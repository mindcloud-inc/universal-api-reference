# DigiParser: Get Document Data



```
GET https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/get-document-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DigiParser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/get-document-data?connectionId=$CONNECTION_ID&parserId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parserId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/get-document-data?${params}`, {
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
| `parserId` | string | yes | Parser UUID from DigiParser Parser Settings -> General Settings. |
| `documentId` | string | no | Document UUID returned by a DigiParser upload response. |
| `externalId` | string | no | External tracking ID provided during upload. Use this instead of Document ID when you do not have the DigiParser document UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Extracted parser fields keyed by DigiParser field name. |
| `metadata` | object | Document metadata including IDs, URLs, processing state, timestamps, and file details. |

## Native endpoint

Through the native DigiParser API, this operation is `GET /api/v1/process/:parserId/files/data` (base URL `https://app.digiparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-data.md) for the provider-specific parameters and requirements.

