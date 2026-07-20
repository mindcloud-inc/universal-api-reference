# validTo: Create Bulk Validation List

Creates a bulk validation list in validTo.

```
POST https://connect.mindcloud.co/v1/universal/validTo/latest/actions/create-bulk-validation-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a validTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/validTo/latest/actions/create-bulk-validation-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "local_file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/validTo/latest/actions/create-bulk-validation-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "local_file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `local_file` | file | yes |  |
| `autoVerify` | boolean | no | Automatically start verification after upload when supported. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_id` | string | The job_id corresponding to the list that was created. |
| `message` | string | Describes API result. |
| `success` | boolean | Whether the API request call was successful. |

## Native endpoint

Through the native validTo API, this operation is `POST /bulk` (base URL `https://api.validto.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-validation-list.md) for the provider-specific parameters and requirements.

