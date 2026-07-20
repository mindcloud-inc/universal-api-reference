# Zenclass: Delete student

Deletes an existing student profile from Zenclass.

```
DELETE https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/delete-student
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenclass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/delete-student?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenclass/latest/actions/delete-student?${params}`, {
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
| `email` | string | yes | Student email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | boolean | Whether the delete request succeeded. |

## Native endpoint

Through the native Zenclass API, this operation is `DELETE /api/v1/student` (base URL `https://api.zenclass.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-student.md) for the provider-specific parameters and requirements.

