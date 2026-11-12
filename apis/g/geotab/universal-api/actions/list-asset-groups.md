# Geotab: List Asset Groups



```
GET https://connect.mindcloud.co/v1/universal/geotab/latest/actions/list-asset-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geotab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geotab/latest/actions/list-asset-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geotab/latest/actions/list-asset-groups?${params}`, {
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
| `search` | object | no | Optional asset group search criteria. |
| `search.id` | string | no | Return the asset group with this ID. |
| `search.name` | string | no | Search asset groups by name. Use % as a wildcard. |
| `search.reference` | string | no | Search asset groups by reference. Use % as a wildcard. |
| `search.includeAllTrees` | boolean | no | Include security and private-user group trees in addition to company groups. |
| `resultsLimit` | number | no |  |
| `sort` | object | no |  |
| `propertySelector` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Geotab API returns.

## Native endpoint

Through the native Geotab API, this operation is `POST` (base URL `https://{{credentials.server}}/apiv1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-asset-groups.md) for the provider-specific parameters and requirements.

