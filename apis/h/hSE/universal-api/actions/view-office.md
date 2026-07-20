# 4HSE: View Office

Retrieves an office from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/view-office
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/view-office?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/view-office?${params}`, {
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
| `id` | string | yes | The office_id to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 4HSE API returns.

## Native endpoint

Through the native 4HSE API, this operation is `GET /v2/office/view/:id` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-office.md) for the provider-specific parameters and requirements.

