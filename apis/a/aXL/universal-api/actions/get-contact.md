# AXL: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AXL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes |  |
| `fields` | string | no | Default: `{id,firstName,lastName,email,phone,createdDate,updatedDate}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AXL API returns.

## Native endpoint

Through the native AXL API, this operation is `GET /crm/lead/:id` (base URL `https://app.axl.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

