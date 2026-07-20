# KYVE: Get Tokenize Share Record Rewards



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-tokenize-share-record-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-tokenize-share-record-rewards?connectionId=$CONNECTION_ID&ownerAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ownerAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-tokenize-share-record-rewards?${params}`, {
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
| `ownerAddress` | string | yes | Owner address to query tokenize share record rewards for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rewards": [
        {}
      ],
      "total": [
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
| `rewards` | array<object> |  |
| `total` | array<object> |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/liquid/v1beta1/{owner_address}/tokenize_share_record_rewards` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tokenize-share-record-rewards.md) for the provider-specific parameters and requirements.

