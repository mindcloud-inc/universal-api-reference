# Imagior: Retrieve Account Details

Retrieves account details from Imagior.

```
GET https://connect.mindcloud.co/v1/universal/imagior/latest/actions/retrieve-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Imagior `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imagior/latest/actions/retrieve-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imagior/latest/actions/retrieve-account-details?${params}`, {
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
      "requestCompletionTime": "string",
      "status": "string",
      "statusCode": 1,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestCompletionTime` | string | Time it took to complete the request. |
| `status` | string | Indicates whether the request was successful. |
| `statusCode` | number | HTTP-style success code returned by Imagior. |
| `timestamp` | date | When the request completed. |
| `usage` | object | Remaining credit information. |

## Native endpoint

Through the native Imagior API, this operation is `GET /user/account` (base URL `https://api.imagior.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-account-details.md) for the provider-specific parameters and requirements.

