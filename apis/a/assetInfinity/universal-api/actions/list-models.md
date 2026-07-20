# Asset Infinity: List Models

Retrieves models from Asset Infinity.

```
GET https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asset Infinity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/list-models?${params}`, {
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
      "data": [
        {
          "createdBy": "string",
          "createdDate": "2026-05-07T12:00:00.000Z",
          "modelId": 1,
          "modelName": "Ava Chen",
          "rowIndexNumber": 1
        }
      ],
      "isSuccess": true,
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].createdBy` | string |  |
| `data[].createdDate` | date |  |
| `data[].modelId` | number |  |
| `data[].modelName` | string |  |
| `data[].rowIndexNumber` | number |  |
| `isSuccess` | boolean |  |
| `message` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native Asset Infinity API, this operation is `GET ModelList` (base URL `https://api.assetinfinity.io/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

