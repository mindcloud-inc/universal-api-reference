# CraftMyPDF: List template versions

Retrieves template versions from your CraftMyPDF account.

```
GET https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/list-template-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/list-template-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/list-template-versions?${params}`, {
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
| `templateId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "referenceId": "string",
      "status": "string",
      "versions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `referenceId` | string |  |
| `status` | string |  |
| `versions` | array<object> |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `GET /list-template-versions` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-versions.md) for the provider-specific parameters and requirements.

