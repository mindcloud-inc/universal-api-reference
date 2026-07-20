# ActiveTrail: Get Mailing List

Retrieves a mailing list from ActiveTrail.

```
GET https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/get-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveTrail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/get-mailing-list?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/get-mailing-list?${params}`, {
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
| `id` | number | yes | Mailing list id. Can be found using the mailing lists endpoint or in the UI. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveTrail API returns.

## Native endpoint

Through the native ActiveTrail API, this operation is `GET /mailinglist/:id` (base URL `https://webapi.mymarketing.co.il/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mailing-list.md) for the provider-specific parameters and requirements.

