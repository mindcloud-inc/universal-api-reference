# DataScope Forms: List Answers with Metadata

Retrieves submitted answers with metadata from DataScope Forms.

```
GET https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-answers-with-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataScope Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-answers-with-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-answers-with-metadata?${params}`, {
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
| `end` | string | no | End of the date range to fetch answers for. |
| `formId` | string | no | Filter answers to a specific DataScope form. |
| `locationId` | string | no | Filter answers to a specific location. |
| `start` | string | no | Start of the date range to fetch answers for. |
| `userId` | string | no | Filter answers to a specific user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "assign_id": "string",
      "assign_internal_id": "string",
      "assign_location_code": "string",
      "assign_location_description": "string",
      "assign_location_name": "Ava Chen",
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "form_answer_id": 1,
      "form_id": 1,
      "form_name": "Ava Chen",
      "form_state": "string",
      "latitude": 1,
      "longitude": 1,
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> | Question-level answers with metadata. |
| `assign_id` | string | Assignment identifier. |
| `assign_internal_id` | string | Internal assignment identifier. |
| `assign_location_code` | string | Assignment location code. |
| `assign_location_description` | string | Assignment location description. |
| `assign_location_name` | string | Assignment location name. |
| `code` | string | Public identifier returned in the DataScope example payload. |
| `created_at` | date | When the form was received. |
| `form_answer_id` | number | Internal code of the form answer. |
| `form_id` | number | Internal code of the form. |
| `form_name` | string | Name of the form. |
| `form_state` | string | Last status of the form answer. |
| `latitude` | number | Latitude where the form was answered. |
| `longitude` | number | Longitude where the form was answered. |
| `user_name` | string | Name of the user. |

## Native endpoint

Through the native DataScope Forms API, this operation is `GET /external/answers` (base URL `https://www.mydatascope.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-answers-with-metadata.md) for the provider-specific parameters and requirements.

