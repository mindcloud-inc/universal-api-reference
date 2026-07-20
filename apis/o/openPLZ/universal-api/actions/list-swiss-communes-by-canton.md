# OpenPLZ: List Swiss Communes by Canton



```
GET https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/list-swiss-communes-by-canton
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenPLZ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/list-swiss-communes-by-canton?connectionId=$CONNECTION_ID&limit=25&offset=0&key=19" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "key": "19"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openPLZ/latest/actions/list-swiss-communes-by-canton?${params}`, {
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
| `key` | string | yes | Swiss canton key. Default: `19`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canton": {},
      "district": {},
      "historicalCode": "string",
      "key": "string",
      "name": "Ava Chen",
      "shortName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canton` | object |  |
| `district` | object |  |
| `historicalCode` | string |  |
| `key` | string |  |
| `name` | string |  |
| `shortName` | string |  |

## Native endpoint

Through the native OpenPLZ API, this operation is `GET /ch/Cantons/{key}/Communes` (base URL `https://openplzapi.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-swiss-communes-by-canton.md) for the provider-specific parameters and requirements.

