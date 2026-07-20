# Explara: Attendee Form

Retrieves an attendee form from Explara.

```
GET https://connect.mindcloud.co/v1/universal/explara/latest/actions/attendee-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/explara/latest/actions/attendee-form?connectionId=$CONNECTION_ID&orderNo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderNo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/explara/latest/actions/attendee-form?${params}`, {
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
| `orderNo` | string | yes | Explara order number. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Explara API returns.

## Native endpoint

Through the native Explara API, this operation is `POST /api/publisher/attendee-form` (base URL `https://www.explara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attendee-form.md) for the provider-specific parameters and requirements.

