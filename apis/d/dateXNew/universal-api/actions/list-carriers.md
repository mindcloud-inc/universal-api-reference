# DateX: List Carriers



```
GET https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-carriers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-carriers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-carriers?${params}`, {
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
| `filters.carrierName` | string | no | Filter carriers by full carrier name. |
| `filters.carrierShortName` | string | no | Filter carriers by short name. |
| `filters.scac` | string | no | Filter carriers by SCAC code. |
| `filters.carrierId` | number | no | Filter carriers by numeric carrier ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrierId": 1,
      "createdOn": "string",
      "customFields": [
        {}
      ],
      "name": "Ava Chen",
      "scac": "string",
      "services": [
        {}
      ],
      "shortName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrierId` | number |  |
| `createdOn` | string |  |
| `customFields` | array<object> |  |
| `name` | string |  |
| `scac` | string |  |
| `services` | array<object> |  |
| `shortName` | string |  |

## Native endpoint

Through the native DateX API, this operation is `POST carriers/get` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-carriers.md) for the provider-specific parameters and requirements.

