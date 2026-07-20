# Bridge: Get Item

Retrieves an item from Bridge.

```
GET https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-item?connectionId=$CONNECTION_ID&userAccessToken=string&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userAccessToken": "string",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-item?${params}`, {
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
| `userAccessToken` | string | yes | Bridge user access token returned by the Authorization token action. |
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountTypes": "string",
      "authenticationExpiresAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastSuccessfulRefresh": "2026-05-07T12:00:00.000Z",
      "lastTryRefresh": "2026-05-07T12:00:00.000Z",
      "providerId": 1,
      "status": 1,
      "statusCodeDescription": "string",
      "statusCodeInfo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountTypes` | string | Account types synchronized on an item. It impacts the available data and the user experience. |
| `authenticationExpiresAt` | date | Timestamp indicating when the Strong Customer Authentication (SCA) will expire |
| `createdAt` | date | Timestamp recording when the item was created |
| `id` | number | Item's unique identifier |
| `lastSuccessfulRefresh` | date | Timestamp recording when the item was last refreshed in success |
| `lastTryRefresh` | date | Timestamp recording when the item was last refreshed |
| `providerId` | number | Provider's unique identifier |
| `status` | number | Represents the overall state of the connection |
| `statusCodeDescription` | string | Description used in the connect session to guide the user on what they need to do |
| `statusCodeInfo` | string | Details the state of the connection |

## Native endpoint

Through the native Bridge API, this operation is `GET /aggregation/items/:id` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

