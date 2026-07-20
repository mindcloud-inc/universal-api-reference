# EducateMe: Delete Course

Deletes an existing course from EducateMe.

```
DELETE https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/delete-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/delete-course?connectionId=$CONNECTION_ID&id=cmnf0cazqnlbh0874pw6w1bs8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "cmnf0cazqnlbh0874pw6w1bs8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/delete-course?${params}`, {
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
| `id` | string | yes | Course ID. Example: `cmnf0cazqnlbh0874pw6w1bs8`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native EducateMe API, this operation is `DELETE /courses/:id` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-course.md) for the provider-specific parameters and requirements.

