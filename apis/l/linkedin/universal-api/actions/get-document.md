# LinkedIn: Get Document

Retrieves a document from LinkedIn.

```
GET https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-document?connectionId=$CONNECTION_ID&documentUrn=urn%253Ali%253Adocument%253AD4D10AQEMykH-I0dW5Q" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentUrn": "urn%3Ali%3Adocument%3AD4D10AQEMykH-I0dW5Q"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-document?${params}`, {
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
| `documentUrn` | string | yes | Example: `urn%3Ali%3Adocument%3AD4D10AQEMykH-I0dW5Q`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "owner": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `owner` | string |  |
| `status` | string |  |

## Native endpoint

Through the native LinkedIn API, this operation is `GET /rest/documents/:documentUrn` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

