# Graphor: Get Source Elements By Type

Retrieves parsed source elements from Graphor by element type.

```
GET https://connect.mindcloud.co/v1/universal/graphor/latest/actions/get-source-elements-by-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Graphor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphor/latest/actions/get-source-elements-by-type?connectionId=$CONNECTION_ID&fileId=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphor/latest/actions/get-source-elements-by-type?${params}`, {
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
| `fileId` | string | yes | The source file identifier whose parsed elements should be returned. |
| `page` | string | no | 1-based page number for element pagination. |
| `pageSize` | string | no | Number of elements to return per page. |
| `type` | string | yes | Optional element type filter such as NarrativeText, Title, or Table. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "page": 1,
      "pageSize": 1,
      "total": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `page` | number |  |
| `pageSize` | number |  |
| `total` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Graphor API, this operation is `GET /get-elements` (base URL `https://sources.graphorlm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-source-elements-by-type.md) for the provider-specific parameters and requirements.

