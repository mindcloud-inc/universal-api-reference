# RapidoForm: List Forms

Retrieves all available forms from RapidoForm.

```
GET https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RapidoForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/list-forms?${params}`, {
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
| `page` | number | no | Page number to retrieve. |
| `surveyId` | string | no |  |
| `status` | string | no | Only return forms with the selected status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "Id": 1,
      "status": "string",
      "surveyName": "Ava Chen",
      "totalQuestion": 1,
      "totalResponses": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `Id` | number |  |
| `status` | string |  |
| `surveyName` | string |  |
| `totalQuestion` | number |  |
| `totalResponses` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native RapidoForm API, this operation is `GET /api/surveys` (base URL `https://www.rapidoform.com/be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

