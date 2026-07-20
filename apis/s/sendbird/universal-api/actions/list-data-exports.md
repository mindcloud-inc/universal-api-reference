# Sendbird: List Data Exports



```
GET https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/list-data-exports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendbird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/list-data-exports?connectionId=$CONNECTION_ID&dataType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/list-data-exports?${params}`, {
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
| `dataType` | string | yes | The export data type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "dataType": "string",
      "requestId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `dataType` | string |  |
| `requestId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Sendbird API, this operation is `GET /export/:dataType` (base URL `https://api-{{credentials.applicationId}}.sendbird.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-exports.md) for the provider-specific parameters and requirements.

