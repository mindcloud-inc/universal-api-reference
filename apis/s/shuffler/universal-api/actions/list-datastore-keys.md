# Shuffler: List Datastore Keys

Retrieves datastore keys from Shuffler.

```
GET https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-datastore-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-datastore-keys?connectionId=$CONNECTION_ID&orgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-datastore-keys?${params}`, {
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
| `orgId` | string | yes | Org Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "keys": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keys` | array |  |
| `success` | boolean |  |

## Native endpoint

Through the native Shuffler API, this operation is `GET /orgs/{orgId}/list_cache` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datastore-keys.md) for the provider-specific parameters and requirements.

