# Dialpad: List Call Centers



```
GET https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-call-centers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-call-centers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-call-centers?${params}`, {
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
| `officeId` | number | no | Filter call centers by Dialpad office ID. Example: `6115773416611840`. |
| `nameSearch` | string | no | Filter call centers by name substring. Example: `Support`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Pagination cursor from a previous Dialpad call centers response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availabilityStatus": "string",
      "country": "string",
      "firstAction": "string",
      "groupDescription": "string",
      "id": "string",
      "name": "Ava Chen",
      "noOperatorsAction": "string",
      "officeId": "string",
      "phoneNumbers": [
        [
          "string"
        ]
      ],
      "state": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availabilityStatus` | string |  |
| `country` | string |  |
| `firstAction` | string |  |
| `groupDescription` | string |  |
| `id` | string |  |
| `name` | string |  |
| `noOperatorsAction` | string |  |
| `officeId` | string |  |
| `phoneNumbers[]` | array<string> |  |
| `state` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Dialpad API, this operation is `GET /callcenters` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-call-centers.md) for the provider-specific parameters and requirements.

