# Damstra Forms: Create Draft Form

Creates a draft form in Damstra Forms.

```
POST https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/create-draft-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/create-draft-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "draftTemplateId": 1,
  "projectId": 1,
  "createdByUserId": 1,
  "fields[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/create-draft-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "draftTemplateId": 1,
    "projectId": 1,
    "createdByUserId": 1,
    "fields[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `draftTemplateId` | number | yes | Draft template identifier for the new form. |
| `projectId` | number | yes | Project identifier for the new form. |
| `createdByUserId` | number | yes | User identifier to record as the form creator. |
| `fields[]` | array<object> | yes | Field values for the form, using Damstra field_reference values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "href": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `href` | string | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `POST /forms` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-form.md) for the provider-specific parameters and requirements.

