# ComPDFKit PDF Editor: PNG to PDF Task



```
GET https://connect.mindcloud.co/v1/universal/comPDFKitPDFEditor/latest/actions/p-ng-to-pdf-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ComPDFKit PDF Editor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comPDFKitPDFEditor/latest/actions/p-ng-to-pdf-task?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comPDFKitPDFEditor/latest/actions/p-ng-to-pdf-task?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {},
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `data` | object |  |
| `msg` | string |  |

## Native endpoint

Through the native ComPDFKit PDF Editor API, this operation is `GET /server/v1/task/png/pdf` (base URL `https://api-server.compdf.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/p-ng-to-pdf-task.md) for the provider-specific parameters and requirements.

