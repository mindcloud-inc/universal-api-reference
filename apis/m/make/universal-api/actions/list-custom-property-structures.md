# Make: List Custom Property Structures

Lists custom property structures for the specified organization.

```
GET https://connect.mindcloud.co/v1/universal/make/latest/actions/list-custom-property-structures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Make `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/make/latest/actions/list-custom-property-structures?connectionId=$CONNECTION_ID&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/make/latest/actions/list-custom-property-structures?${params}`, {
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
| `organizationId` | number | yes | The ID of the Make organization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "belongers": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `belongers` | array<object> |  |
| `created` | date |  |
| `id` | number |  |

## Native endpoint

Through the native Make API, this operation is `GET /custom-property-structures` (base URL `https://us2.make.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-property-structures.md) for the provider-specific parameters and requirements.

