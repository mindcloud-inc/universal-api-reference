# Oanda: Get Dataset

Retrieves exchange-rate dataset details from Oanda.

```
GET https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oanda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-dataset?connectionId=$CONNECTION_ID&data_set=OANDA&ext=json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data_set": "OANDA",
  "ext": "json"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-dataset?${params}`, {
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
| `data_set` | string | yes | Dataset code. Default: `OANDA`. |
| `ext` | string | yes | Response format. Default: `json`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datasets": [
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
| `datasets` | array<object> | Dataset details including quotables and cross currency. |

## Native endpoint

Through the native Oanda API, this operation is `GET /v2/datasets/:data_set.:ext` (base URL `https://exchange-rates-api.oanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dataset.md) for the provider-specific parameters and requirements.

