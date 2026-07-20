# KYVE: Get Tokenize Share Record By Denom



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-tokenize-share-record-by-denom
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-tokenize-share-record-by-denom?connectionId=$CONNECTION_ID&denom=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "denom": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-tokenize-share-record-by-denom?${params}`, {
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
| `denom` | string | yes | Tokenized share denomination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "record": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `record` | object |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/liquid/v1beta1/tokenize_share_record_by_denom/{denom}` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tokenize-share-record-by-denom.md) for the provider-specific parameters and requirements.

