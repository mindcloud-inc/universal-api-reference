# OpenSea: Build Mint Transaction Data For Drop

Builds mint transaction data for an OpenSea drop.

```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/build-drop-mint-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/build-drop-mint-transaction?connectionId=$CONNECTION_ID&slug=string&minter=string&quantity=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string",
  "minter": "string",
  "quantity": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/build-drop-mint-transaction?${params}`, {
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
| `slug` | string | yes | The collection slug identifying the drop |
| `minter` | string | yes | Wallet address that will receive the minted tokens |
| `quantity` | number | yes | Number of tokens to mint |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native OpenSea API, this operation is `POST /api/v2/drops/{slug}/mint` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/build-drop-mint-transaction.md) for the provider-specific parameters and requirements.

