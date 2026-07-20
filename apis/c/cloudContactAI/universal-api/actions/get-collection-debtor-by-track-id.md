# CloudContactAI: Get Collection Debtor by Track ID



```
GET https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/get-collection-debtor-by-track-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/get-collection-debtor-by-track-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/get-collection-debtor-by-track-id?${params}`, {
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
| `trackId` | string | no | The debtor track ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "debtor": {},
      "status": "string",
      "trackId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `debtor` | object |  |
| `status` | string |  |
| `trackId` | string |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `GET api/v2/collection/debtor/:trackId` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection-debtor-by-track-id.md) for the provider-specific parameters and requirements.

