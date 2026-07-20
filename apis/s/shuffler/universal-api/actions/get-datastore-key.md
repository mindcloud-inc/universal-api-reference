# Shuffler: Get Datastore Key

Retrieves a datastore key from Shuffler.

```
GET https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/get-datastore-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/get-datastore-key?connectionId=$CONNECTION_ID&key=string&orgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string",
  "orgId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/get-datastore-key?${params}`, {
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
| `category` | string | no | Optional datastore category. |
| `key` | string | yes | Datastore key. |
| `orgId` | string | yes | Org Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "executionId": "string",
      "key": "string",
      "success": true,
      "value": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `executionId` | string |  |
| `key` | string |  |
| `success` | boolean |  |
| `value` | string |  |
| `workflowId` | string |  |

## Native endpoint

Through the native Shuffler API, this operation is `POST /orgs/{orgId}/get_cache` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datastore-key.md) for the provider-specific parameters and requirements.

