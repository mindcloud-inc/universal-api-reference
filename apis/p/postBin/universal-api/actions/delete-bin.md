# PostBin: Delete Bin

Deletes a PostBin bin and its requests.

```
DELETE https://connect.mindcloud.co/v1/universal/postBin/latest/actions/delete-bin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostBin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/postBin/latest/actions/delete-bin?connectionId=$CONNECTION_ID&binId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "binId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postBin/latest/actions/delete-bin?${params}`, {
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
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string | Deletion status message. |

## Native endpoint

Through the native PostBin API, this operation is `DELETE /bin/:binId` (base URL `https://www.postb.in/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bin.md) for the provider-specific parameters and requirements.

