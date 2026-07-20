# Startquestion: Create Mailing

Creates a survey mailing in Startquestion.

```
POST https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/create-mailing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Startquestion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/create-mailing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": 1,
  "templateId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/startquestion/latest/actions/create-mailing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": 1,
    "templateId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | number | yes | Survey ID. |
| `templateId` | number | yes | Template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id_mailing": "string",
      "receivers": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id_mailing` | string | Created mailing ID. |
| `receivers` | number | Number of recipients. |

## Native endpoint

Through the native Startquestion API, this operation is `POST /mailing/create` (base URL `https://www.startquestion.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mailing.md) for the provider-specific parameters and requirements.

