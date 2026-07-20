# EMnify: List Application Tokens

Retrieves a list of application tokens from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-application-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-application-tokens?connectionId=$CONNECTION_ID&limit=25&offset=0&authToken=Paste%20the%20auth_token%20from%20Retrieve%20Authentication%20Token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "authToken": "Paste the auth_token from Retrieve Authentication Token"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-application-tokens?${params}`, {
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
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. Example: `Paste the auth_token from Retrieve Authentication Token`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "creator": {
        "id": 1,
        "name": "Ava Chen",
        "username": "Ava Chen"
      },
      "description": "string",
      "id": 1,
      "status": {
        "description": "string",
        "id": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `creator.id` | number |  |
| `creator.name` | string |  |
| `creator.username` | string |  |
| `description` | string |  |
| `id` | number |  |
| `status.description` | string |  |
| `status.id` | number |  |

## Native endpoint

Through the native EMnify API, this operation is `GET /application_token` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-application-tokens.md) for the provider-specific parameters and requirements.

