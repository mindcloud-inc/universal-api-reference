# Smarty-streets: Suggest International Addresses

Finds international address suggestions in Smarty-streets by search text.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/suggest-international-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/suggest-international-addresses?connectionId=$CONNECTION_ID&country=FRA&search=1%20rue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "FRA",
  "search": "1 rue"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/suggest-international-addresses?${params}`, {
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
| `country` | string | yes | ISO3 country code for the desired address. Default: `FRA`. Example: `FRA`. |
| `search` | string | yes | Address text typed so far. Default: `1 rue`. Example: `1 rue`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Smarty-streets API returns.

## Native endpoint

Through the native Smarty-streets API, this operation is `GET https://international-autocomplete.api.smarty.com/v2/lookup` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/suggest-international-addresses.md) for the provider-specific parameters and requirements.

