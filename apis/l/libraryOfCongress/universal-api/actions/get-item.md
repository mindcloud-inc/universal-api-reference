# Library of Congress: Get Item

Retrieves a Library of Congress item.

```
GET https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Library of Congress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/get-item?connectionId=$CONNECTION_ID&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/get-item?${params}`, {
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
| `itemId` | string | yes | The loc.gov item identifier segment, such as 2014717546. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Library of Congress API returns.

## Native endpoint

Through the native Library of Congress API, this operation is `GET /item/{itemId}/` (base URL `https://www.loc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

