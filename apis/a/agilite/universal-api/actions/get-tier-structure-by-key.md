# Agilite: Get Tier Structure By Key

Retrieves tier structure profiles from Agilite by tier keys.

```
GET https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-tier-structure-by-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-tier-structure-by-key?connectionId=$CONNECTION_ID&tierKeys=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tierKeys": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-tier-structure-by-key?${params}`, {
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
| `tierKeys` | string | yes | Comma-separated tier structure keys to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeMetaData` | boolean | no | Whether to include tier metadata. Default: `true`. |
| `includeTierEntries` | boolean | no | Whether to include tier entries. Default: `true`. |
| `includeValues` | boolean | no | Whether to include tier values. Default: `true`. |
| `valuesOutputFormat` | list | no | Value output format. Default: `json`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agilite API returns.

## Native endpoint

Through the native Agilite API, this operation is `GET /tierstructures/getTierByKey` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tier-structure-by-key.md) for the provider-specific parameters and requirements.

