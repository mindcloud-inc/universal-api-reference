# Salesmate: Add Company Note



```
POST https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/add-company-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/add-company-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/add-company-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "note": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Salesmate company ID. |
| `note` | string | yes | Note body in HTML or rich text markup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "noteId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `noteId` | number |  |

## Native endpoint

Through the native Salesmate API, this operation is `POST /company/v4/modules/5/object/:companyId/notes` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-company-note.md) for the provider-specific parameters and requirements.

