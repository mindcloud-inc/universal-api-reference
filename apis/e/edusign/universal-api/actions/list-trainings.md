# Edusign: List Trainings

Retrieves trainings from Edusign.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-trainings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-trainings?connectionId=$CONNECTION_ID&page=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-trainings?${params}`, {
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
| `page` | string | yes | Query param for pagination, starts at page "0" and displays 50 trainings per page |
| `name` | string | no | Filter trainings based on their name |
| `date` | string | no | An array of two dates (start and end) to filter the dates of the training |
| `students` | string | no | Filter trainings based on an array of students ids enrolled in that training |
| `professors` | string | no | An array of professors IDs to filter the professors ids of the training |
| `archived` | string | no | Filters the archived status of the training |
| `creatorId` | string | no | An array of creator IDs to filter the creator of the training |
| `dateCreated` | string | no | An array of two dates (start and end) to filter the date created of the training |
| `dateUpdated` | string | no | An array of two dates (start and end) to filter the date updated of the training |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {
          "apiId": "string",
          "apiType": "string",
          "archived": true,
          "creatorId": "string",
          "dateCreated": "string",
          "dateUpdated": "string",
          "end": "string",
          "goals": "string",
          "id": "string",
          "name": "Ava Chen",
          "schoolId": "string",
          "start": "string",
          "tags": [
            "string"
          ]
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | array<object> |  |
| `result[].apiId` | string |  |
| `result[].apiType` | string |  |
| `result[].archived` | boolean |  |
| `result[].creatorId` | string |  |
| `result[].dateCreated` | string |  |
| `result[].dateUpdated` | string |  |
| `result[].end` | string |  |
| `result[].goals` | string |  |
| `result[].id` | string |  |
| `result[].name` | string |  |
| `result[].schoolId` | string |  |
| `result[].start` | string |  |
| `result[].tags` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/trainings/` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-trainings.md) for the provider-specific parameters and requirements.

