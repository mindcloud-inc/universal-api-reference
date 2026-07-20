# Leadspicker: Get Person Summary

Retrieves a simplified person record from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-person-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-person-summary?connectionId=$CONNECTION_ID&personId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-person-summary?${params}`, {
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
| `personId` | number | yes | Leadspicker person identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar_url": "https://example.com",
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "labels": [
        {}
      ],
      "person_data": {},
      "project_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_url` | string |  |
| `created` | date |  |
| `id` | number |  |
| `labels` | array<object> |  |
| `person_data` | object |  |
| `project_id` | number |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/persons-simple/:person_id` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-summary.md) for the provider-specific parameters and requirements.

