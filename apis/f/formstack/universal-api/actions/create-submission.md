# Formstack: Create Submission

Creates a new submission in Formstack.

```
POST https://connect.mindcloud.co/v1/universal/formstack/latest/actions/create-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/create-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": 1,
  "fields[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstack/latest/actions/create-submission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": 1,
    "fields[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | list<number> | yes | The unique identifier of the form to submit to. |
| `fields[]` | array<object> | yes | Array of field values to submit. |
| `fields[].id` | string | no | The ID of the field to populate. |
| `fields[].value` | object | no | Provide the Formstack typed field-value object. For text fields use `{ "value": "example text" }`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `read` | list<string> | no | Whether to mark the submission as read upon creation. One of: `false`, `true`. |
| `userAgent` | string | no | The browser user agent string of the submitter. |
| `remoteAddr` | string | no | The IP address from which the submission is being made. |
| `latitude` | string | no | The GPS latitude coordinate if location data is available. |
| `longitude` | string | no | The GPS longitude coordinate if location data is available. |
| `deviceId` | string | no | The unique device identifier if available from mobile submissions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "formId": 1,
      "id": 1,
      "latitude": "string",
      "longitude": "string",
      "paymentStatus": "string",
      "remoteAddr": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "userAgent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Array of field data contained in the submission. |
| `formId` | number | The ID of the form this submission belongs to. |
| `id` | number | The ID of the created submission. |
| `latitude` | string | The GPS latitude coordinate if location data was captured. |
| `longitude` | string | The GPS longitude coordinate if location data was captured. |
| `paymentStatus` | string | The current payment status if the form includes payment processing. |
| `remoteAddr` | string | The IP address from which the submission was made. |
| `timestamp` | date | The date and time when the submission was created. |
| `userAgent` | string | The browser user agent string of the submitter. |

## Native endpoint

Through the native Formstack API, this operation is `POST /forms/:formId/submissions` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-submission.md) for the provider-specific parameters and requirements.

