# Fidel API: Get MID

Retrieves a MID from a Fidel program.

```
GET https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-mid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-mid?connectionId=$CONNECTION_ID&programId=string&midId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "programId": "string",
  "midId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-mid?${params}`, {
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
| `programId` | string | yes |  |
| `midId` | string | yes | The MID ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "brandId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isShared": true,
      "live": true,
      "locationId": "string",
      "mastercard": {},
      "programId": "string",
      "scheme": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "visa": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `brandId` | string |  |
| `created` | date |  |
| `id` | string |  |
| `isShared` | boolean |  |
| `live` | boolean |  |
| `locationId` | string |  |
| `mastercard` | object |  |
| `programId` | string |  |
| `scheme` | string |  |
| `updated` | date |  |
| `visa` | object |  |

## Native endpoint

Through the native Fidel API API, this operation is `GET /programs/:programId/mids/:midId` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mid.md) for the provider-specific parameters and requirements.

