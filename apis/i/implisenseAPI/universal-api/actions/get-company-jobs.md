# Implisense: Get Company Jobs

Retrieves company jobs from Implisense API.

```
GET https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Implisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-jobs?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-jobs?${params}`, {
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
| `id` | string | yes | Implisense company identifier, for example DEVFCLQFW054. |
| `since` | string | no | Optional lower timestamp boundary for returned jobs. |
| `size` | number | no | Maximum number of jobs to return. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "publisher": "string",
      "source": "string",
      "text": "string",
      "timestamp": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `publisher` | string |  |
| `source` | string |  |
| `text` | string |  |
| `timestamp` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Implisense API, this operation is `GET /companies/:id/jobs` (base URL `https://german-company-data.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-jobs.md) for the provider-specific parameters and requirements.

