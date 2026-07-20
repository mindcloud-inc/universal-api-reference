# DataScope Forms: List Answers

Retrieves submitted answers from DataScope Forms.

```
GET https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-answers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataScope Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-answers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-answers?${params}`, {
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
| `formId` | number | no | Filter answers to a specific DataScope form. |
| `userId` | string | no | Filter answers to a specific user. |
| `start` | string | no | Start of the date range to fetch answers for. Example: `2026-03-01`. |
| `end` | string | no | End of the date range to fetch answers for. Example: `2026-03-18`. |
| `locationId` | number | no | Filter answers to a specific location. |
| `dateModified` | boolean | no | Use the answer modification date instead of the creation date when filtering. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "form_answer_id": 1,
      "form_id": 1,
      "form_name": "Ava Chen",
      "form_state": "string",
      "latitude": 1,
      "longitude": 1,
      "user_identifier": "string",
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Public identifier returned in the DataScope example payload. |
| `created_at` | date | When the form was received. |
| `form_answer_id` | number | Internal code of the form answer. |
| `form_id` | number | Internal code of the form. |
| `form_name` | string | Name of the form. |
| `form_state` | string | Last status of the form answer. |
| `latitude` | number | Latitude where the form was answered. |
| `longitude` | number | Longitude where the form was answered. |
| `user_identifier` | string | Identifier of the user who submitted the form. |
| `user_name` | string | Name of the user. |

## Native endpoint

Through the native DataScope Forms API, this operation is `GET /external/v2/answers` (base URL `https://www.mydatascope.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-answers.md) for the provider-specific parameters and requirements.

