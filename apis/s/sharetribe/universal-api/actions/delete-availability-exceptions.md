# Sharetribe: Delete Availability Exceptions

Deletes existing availability exceptions from Sharetribe.

```
DELETE https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/delete-availability-exceptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sharetribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/delete-availability-exceptions?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/delete-availability-exceptions?${params}`, {
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
| `id` | string | yes | The ID of the availability exception to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Resource attributes payload. |
| `id` | string | Resource ID. |
| `relationships` | object | Resource relationships payload. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Sharetribe API, this operation is `POST availability_exceptions/delete` (base URL `https://flex-integ-api.sharetribe.com/v1/integration_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-availability-exceptions.md) for the provider-specific parameters and requirements.

