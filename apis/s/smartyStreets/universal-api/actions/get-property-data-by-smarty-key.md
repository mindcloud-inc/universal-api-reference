# Smarty-streets: Get Property Data By SmartyKey

Retrieves property data from Smarty-streets by SmartyKey.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/get-property-data-by-smarty-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/get-property-data-by-smarty-key?connectionId=$CONNECTION_ID&smartyKey=1144020281" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "smartyKey": "1144020281"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/get-property-data-by-smarty-key?${params}`, {
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
| `smartyKey` | string | yes | SmartyKey for the address record. Default: `1144020281`. Example: `1144020281`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Smarty-streets API returns.

## Native endpoint

Through the native Smarty-streets API, this operation is `GET https://us-enrichment.api.smarty.com/lookup/{smartyKey}/property` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-property-data-by-smarty-key.md) for the provider-specific parameters and requirements.

