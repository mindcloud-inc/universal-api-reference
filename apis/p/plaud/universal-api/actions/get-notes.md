# Plaud AI: Get Notes



```
GET https://connect.mindcloud.co/v1/universal/plaud/latest/actions/get-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plaud AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plaud/latest/actions/get-notes?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plaud/latest/actions/get-notes?${params}`, {
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
| `fileId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataContent": "string",
      "dataErrorCode": 1,
      "dataId": "string",
      "dataLink": "https://example.com",
      "dataPath": "string",
      "dataTabName": "Ava Chen",
      "dataTitle": "string",
      "dataType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataContent` | string |  |
| `dataErrorCode` | number |  |
| `dataId` | string |  |
| `dataLink` | string |  |
| `dataPath` | string |  |
| `dataTabName` | string |  |
| `dataTitle` | string |  |
| `dataType` | string |  |

## Native endpoint

Through the native Plaud AI API, this operation is `POST /mcp` (base URL `https://mcp.plaud.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notes.md) for the provider-specific parameters and requirements.

