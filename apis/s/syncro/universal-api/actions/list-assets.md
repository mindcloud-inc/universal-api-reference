# Syncro: List Assets

Retrieves a list of assets from Syncro.

```
GET https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-assets?${params}`, {
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
| `snmpEnabled` | boolean | no | Any assets with SNMP enabled. |
| `customerId` | number | no | Any assets attached to a Customer ID. |
| `assetTypeId` | number | no | Any assets attached to an Asset Type ID. |
| `query` | string | no | Search query. |
| `page` | number | no | Returns the provided page of results. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Syncro API returns.

## Native endpoint

Through the native Syncro API, this operation is `GET /customer_assets` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

