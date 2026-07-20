# MojoTxt: List Subscribers

Retrieves subscribers from MojoTxt.

```
GET https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/list-subscribers?${params}`, {
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
| `emailKnown` | string | no | Set to 1 to return only subscribers with known email addresses. |
| `listId` | string | no | Return only subscribers from a specific subscription list. |
| `nameKnown` | string | no | Set to 1 to return only subscribers with known first names. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Address": "string",
      "City": "string",
      "Email": "ava@example.com",
      "FirstName": "Ava",
      "FirstUsage": 1,
      "id": 1,
      "LastName": "Chen",
      "LastUsage": 1,
      "PhoneNumber": "string",
      "State": "string",
      "Zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address` | string | The subscriber mailing address. |
| `City` | string | The subscriber city. |
| `Email` | string | The subscriber email address. |
| `FirstName` | string | The subscriber first name. |
| `FirstUsage` | number | The UNIX timestamp when the subscriber first interacted with this phone number. |
| `id` | number | The unique identifier for the subscriber. |
| `LastName` | string | The subscriber last name. |
| `LastUsage` | number | The UNIX timestamp when the subscriber most recently interacted with this phone number. |
| `PhoneNumber` | string | The subscriber phone number in international format. |
| `State` | string | The subscriber two-letter state abbreviation. |
| `Zip` | string | The subscriber postal code. |

## Native endpoint

Through the native MojoTxt API, this operation is `GET /subscribers/list` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

