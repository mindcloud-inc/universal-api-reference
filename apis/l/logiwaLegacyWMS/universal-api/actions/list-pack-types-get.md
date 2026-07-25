# Logiwa Legacy WMS: List Pack Types (GET)

By using these endpoints, the users can obtain all the information that is related to the pack types of the items.

To obtain this information, the users should first reach the Pack Type ID values by using the InventoryItemPackTypeSearch endpoint. After this process, the users will be able to use the InventoryItemPackTypeGet endpoint.

```
GET https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-pack-types-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-pack-types-get?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-pack-types-get?${params}`, {
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
| `iD` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logiwa Legacy WMS API returns.

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST /en/api/IntegrationApi/InventoryItemPackTypeGET` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pack-types-get.md) for the provider-specific parameters and requirements.

