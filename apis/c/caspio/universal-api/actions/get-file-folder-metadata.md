# Caspio: Get File Folder Metadata

Retrieves file folder metadata from Caspio.

```
GET https://connect.mindcloud.co/v1/universal/caspio/latest/actions/get-file-folder-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caspio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/get-file-folder-metadata?connectionId=$CONNECTION_ID&externalKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "externalKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caspio/latest/actions/get-file-folder-metadata?${params}`, {
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
| `externalKey` | string | yes | Folder ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | object |  |

## Native endpoint

Through the native Caspio API, this operation is `GET /v3/files/folders/{externalKey}` (base URL `https://d2hbw900.caspio.com/integrations/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-folder-metadata.md) for the provider-specific parameters and requirements.

