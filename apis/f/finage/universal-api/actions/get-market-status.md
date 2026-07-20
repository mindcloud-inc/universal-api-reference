# Finage: Get Market Status

Retrieves market status from Finage.

```
GET https://connect.mindcloud.co/v1/universal/finage/latest/actions/get-market-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finage/latest/actions/get-market-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finage/latest/actions/get-market-status?${params}`, {
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
| `country` | string | no | Country code to check market status for. Example: `US`. |
| `currencies` | boolean | no | Include forex and crypto market status in the response. Default: `true`. |
| `holidays` | boolean | no | Include market holidays for the selected country. Default: `false`. |
| `tradingHours` | boolean | no | Include regular trading hours in the response. Default: `false`. |
| `extendedHours` | boolean | no | Include extended-hours status in the response. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Finage API returns.

## Native endpoint

Through the native Finage API, this operation is `GET /marketstatus` (base URL `https://api.finage.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-market-status.md) for the provider-specific parameters and requirements.

