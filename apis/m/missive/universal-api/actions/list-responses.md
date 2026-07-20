# Missive: List Responses

Retrieves responses from your Missive workspace.

```
GET https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-responses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-responses?${params}`, {
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
| `organization` | string | no | Organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responses": [
        {
          "body": "string",
          "externalId": {},
          "externalSource": {},
          "id": "string",
          "modifiedAt": 1,
          "organization": "string",
          "sharedLabels": {},
          "shareWithTeam": {},
          "subject": {},
          "title": "string",
          "user": {}
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responses[].body` | string |  |
| `responses[].externalId` | object |  |
| `responses[].externalSource` | object |  |
| `responses[].id` | string |  |
| `responses[].modifiedAt` | number |  |
| `responses[].organization` | string |  |
| `responses[].sharedLabels` | object |  |
| `responses[].shareWithTeam` | object |  |
| `responses[].subject` | object |  |
| `responses[].title` | string |  |
| `responses[].user` | object |  |

## Native endpoint

Through the native Missive API, this operation is `GET /responses` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-responses.md) for the provider-specific parameters and requirements.

