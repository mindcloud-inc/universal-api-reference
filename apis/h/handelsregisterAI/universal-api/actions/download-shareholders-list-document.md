# Handelsregister AI: Download Shareholders List Document

Retrieves a shareholders list document from Handelsregister AI.

```
GET https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/download-shareholders-list-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Handelsregister AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/download-shareholders-list-document?connectionId=$CONNECTION_ID&companyId=20a1510e88cd2e9b166db4d0bc5d563d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "20a1510e88cd2e9b166db4d0bc5d563d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/download-shareholders-list-document?${params}`, {
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
| `companyId` | string | yes | Unique company entity ID from search results. Example: `20a1510e88cd2e9b166db4d0bc5d563d`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | PDF bytes returned by the provider. |
| `type` | string | Raw response wrapper type. |

## Native endpoint

Through the native Handelsregister AI API, this operation is `GET /fetch-document` (base URL `https://handelsregister.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-shareholders-list-document.md) for the provider-specific parameters and requirements.

