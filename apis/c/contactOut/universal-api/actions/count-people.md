# ContactOut: Count People

Retrieves a count of people matching search filters in ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/count-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/count-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/count-people?${params}`, {
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
| `company` | string | no | Filter by company. |
| `job_title` | string | no | Filter by job title. |
| `name` | string | no | Match people by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status_code": 1,
      "total_results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status_code` | number |  |
| `total_results` | number |  |

## Native endpoint

Through the native ContactOut API, this operation is `POST /v1/people/count` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-people.md) for the provider-specific parameters and requirements.

