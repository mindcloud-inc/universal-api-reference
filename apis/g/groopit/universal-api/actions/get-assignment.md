# Groopit: Get Assignment



```
GET https://connect.mindcloud.co/v1/universal/groopit/latest/actions/get-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groopit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/groopit/latest/actions/get-assignment?connectionId=$CONNECTION_ID&assignmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assignmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/groopit/latest/actions/get-assignment?${params}`, {
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
      "Id": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | string | Unique Groopit assignment identifier. |
| `Title` | string | Assignment title. |

## Native endpoint

Through the native Groopit API, this operation is `GET /Assignments(:assignmentId)` (base URL `https://app.groopit.co/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-assignment.md) for the provider-specific parameters and requirements.

