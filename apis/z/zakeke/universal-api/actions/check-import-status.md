# Zakeke: Check Import Status



```
GET https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/check-import-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zakeke `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/check-import-status?connectionId=$CONNECTION_ID&taskID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/check-import-status?${params}`, {
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
| `taskID` | number | yes | Task identifier returned by Import Products Via CSV. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorOccurred": true,
      "importedProducts": [
        {
          "hasConfiguredArea": true,
          "productID": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorOccurred` | boolean |  |
| `importedProducts[].hasConfiguredArea` | boolean |  |
| `importedProducts[].productID` | string |  |

## Native endpoint

Through the native Zakeke API, this operation is `GET /v2/csv/importingresult/:taskID` (base URL `https://api.zakeke.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-import-status.md) for the provider-specific parameters and requirements.

