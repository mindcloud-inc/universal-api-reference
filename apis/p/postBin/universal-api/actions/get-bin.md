# PostBin: Get Bin

Retrieves a PostBin bin by ID.

```
GET https://connect.mindcloud.co/v1/universal/postBin/latest/actions/get-bin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostBin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postBin/latest/actions/get-bin?connectionId=$CONNECTION_ID&binId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "binId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postBin/latest/actions/get-bin?${params}`, {
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
| `binId` | string | yes | The PostBin bin identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "binId": "string",
      "expires": 1,
      "now": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `binId` | string | Opaque identifier for the temporary bin. |
| `expires` | number | UTC timestamp in milliseconds when the bin expires. |
| `now` | number | UTC timestamp in milliseconds when the bin was created. |

## Native endpoint

Through the native PostBin API, this operation is `GET /bin/:binId` (base URL `https://www.postb.in/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bin.md) for the provider-specific parameters and requirements.

