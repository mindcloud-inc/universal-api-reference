# Lodgify: List Availability

Retrieves availability calendar data from Lodgify.

```
GET https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/list-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lodgify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/list-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/list-availability?${params}`, {
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
| `propertyId` | number | no | Example: `779887`. |
| `roomTypeId` | number | no | Example: `847029`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "periods": [
        {}
      ],
      "propertyId": 1,
      "roomTypeId": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `periods` | array<object> |  |
| `propertyId` | number |  |
| `roomTypeId` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native Lodgify API, this operation is `GET /v2/availability` (base URL `https://api.lodgify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-availability.md) for the provider-specific parameters and requirements.

