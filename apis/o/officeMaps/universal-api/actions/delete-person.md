# OfficeMaps: Delete Person

Deletes an existing person from OfficeMaps.

```
DELETE https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/delete-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeMaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/delete-person?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/delete-person?${params}`, {
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
| `id` | string | yes | Person UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failure": true,
      "messages": [
        "string"
      ],
      "notFound": true,
      "success": true,
      "unauthorized": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failure` | boolean | Whether the request failed. |
| `messages` | array<string> | Provider messages when returned. |
| `notFound` | boolean | Whether the target record was not found. |
| `success` | boolean | Whether the request succeeded. |
| `unauthorized` | boolean | Whether the request was unauthorized. |

## Native endpoint

Through the native OfficeMaps API, this operation is `DELETE /v1/person/:id` (base URL `https://api.officemaps.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-person.md) for the provider-specific parameters and requirements.

