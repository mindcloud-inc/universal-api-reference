# Groopit: List Assignment Posts



```
GET https://connect.mindcloud.co/v1/universal/groopit/latest/actions/list-assignment-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groopit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/groopit/latest/actions/list-assignment-posts?connectionId=$CONNECTION_ID&assignmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assignmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/groopit/latest/actions/list-assignment-posts?${params}`, {
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
| `assignmentId` | string | yes | Groopit assignment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreatorEmail": "ava@example.com",
      "CreatorId": "string",
      "Id": "string",
      "Timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatorEmail` | string | Creator email when present. |
| `CreatorId` | string | Groopit creator identifier when present. |
| `Id` | string | Unique Groopit post identifier. |
| `Timestamp` | date | When the post was created. |

## Native endpoint

Through the native Groopit API, this operation is `GET /Assignments(:assignmentId)/Posts` (base URL `https://app.groopit.co/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assignment-posts.md) for the provider-specific parameters and requirements.

