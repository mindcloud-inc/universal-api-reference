# CentralStationCRM: Get Current User

Retrieves the current user from CentralStationCRM.

```
GET https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CentralStationCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        "string"
      ],
      "currentAccount": "string",
      "first": "string",
      "id": 1,
      "last": "string",
      "name": "Ava Chen",
      "salutationFormal": "string",
      "salutationInformal": "string",
      "salutationOfficial": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<string> |  |
| `currentAccount` | string |  |
| `first` | string |  |
| `id` | number |  |
| `last` | string |  |
| `name` | string |  |
| `salutationFormal` | string |  |
| `salutationInformal` | string |  |
| `salutationOfficial` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native CentralStationCRM API, this operation is `GET /api/user` (base URL `https://api.centralstationcrm.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

