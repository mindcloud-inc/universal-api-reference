# Hireflix: List Position Interviews

Retrieves interviews for a position in Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-position-interviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-position-interviews?connectionId=$CONNECTION_ID&variables.id=string&variables.limit=50&variables.direction=FORWARD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string",
  "variables.limit": "50",
  "variables.direction": "FORWARD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-position-interviews?${params}`, {
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
| `variables.id` | string | yes | The Hireflix position ID. |
| `variables.limit` | number | yes | The number of interviews to return per page. Default: `50`. |
| `variables.direction` | string | yes | The pagination direction. Use FORWARD for the next page or BACKWARD for the previous page. Default: `FORWARD`. |
| `variables.lastCursor` | string | no | The pagination cursor from the previous result page. |
| `variables.filterId` | string | no | Filter interviews by interview ID. |
| `variables.filterEmail` | string | no | Filter interviews by candidate email. |
| `variables.filterFirstName` | string | no | Filter interviews by candidate first name. |
| `variables.filterLastName` | string | no | Filter interviews by candidate last name. |
| `variables.filterStatus` | string | no | Filter interviews by Hireflix status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "lastCursor": "string",
      "results": [
        {
          "candidate": {
            "email": "ava@example.com",
            "firstName": "Ava",
            "lastName": "Chen",
            "phone": "string"
          },
          "createdAt": 1,
          "expires": 1,
          "externalId": "string",
          "id": "string",
          "score": {
            "type": "string",
            "value": 1
          },
          "status": "string",
          "updatedAt": 1
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `lastCursor` | string |  |
| `results[].candidate.email` | string |  |
| `results[].candidate.firstName` | string |  |
| `results[].candidate.lastName` | string |  |
| `results[].candidate.phone` | string |  |
| `results[].createdAt` | number |  |
| `results[].expires` | number |  |
| `results[].externalId` | string |  |
| `results[].id` | string |  |
| `results[].score.type` | string |  |
| `results[].score.value` | number |  |
| `results[].status` | string |  |
| `results[].updatedAt` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-position-interviews.md) for the provider-specific parameters and requirements.

