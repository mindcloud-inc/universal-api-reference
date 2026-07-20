# Xola: Get Experience Availability

Retrieves availability for an experience from Xola.

```
GET https://connect.mindcloud.co/v1/universal/xola/latest/actions/get-experience-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xola `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xola/latest/actions/get-experience-availability?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xola/latest/actions/get-experience-availability?${params}`, {
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
| `id` | string | yes | Experience identifier from Xola. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability[]` | array<object> | Availability slots returned by Xola for a single experience. |

## Native endpoint

Through the native Xola API, this operation is `GET /experiences/{id}/availability` (base URL `https://sandbox.xola.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-experience-availability.md) for the provider-specific parameters and requirements.

