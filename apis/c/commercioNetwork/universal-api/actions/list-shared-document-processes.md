# CommercioNetwork: List Shared Document Processes

Retrieves shared document processes from CommercioNetwork.

```
GET https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/list-shared-document-processes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CommercioNetwork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/list-shared-document-processes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commercioNetwork/latest/actions/list-shared-document-processes?${params}`, {
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
      "paging": {},
      "processes": [
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
| `paging` | object | Cursor pagination metadata from the provider. |
| `processes` | array<object> | The shared document processes visible to the account. |

## Native endpoint

Through the native CommercioNetwork API, this operation is `GET /sharedoc/process` (base URL `https://dev-api.commercio.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shared-document-processes.md) for the provider-specific parameters and requirements.

