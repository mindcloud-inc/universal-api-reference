# RemOnline: Get Person By ID

Retrieves a person from RemOnline by ID.

```
GET https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/get-person-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RemOnline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/get-person-by-id?connectionId=$CONNECTION_ID&person_id=38077743" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "person_id": "38077743"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/get-person-by-id?${params}`, {
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
| `person_id` | number | yes | ID of the person. Example: `38077743`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RemOnline API returns.

## Native endpoint

Through the native RemOnline API, this operation is `GET /v2/contacts/people/:person_id` (base URL `https://api.roapp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-by-id.md) for the provider-specific parameters and requirements.

