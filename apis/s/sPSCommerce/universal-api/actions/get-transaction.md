# SPS Commerce: Get Transaction

Retrieve a specific file.

```
GET https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SPS Commerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/get-transaction?connectionId=$CONNECTION_ID&filePath=testout%2FfileName.dat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filePath": "testout/fileName.dat"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/get-transaction?${params}`, {
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
| `filePath` | string | yes | Full absolute path to the file (case sensitive). Example: `testout/fileName.dat`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SPS Commerce API returns.

## Native endpoint

Through the native SPS Commerce API, this operation is `GET transactions/v5/data/:filePath` (base URL `https://api.spscommerce.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

