# GetSales.io: Add Contact To Automation



```
PUT https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/add-contact-to-automation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/add-contact-to-automation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "flowUuid": "string",
  "leadUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/add-contact-to-automation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "flowUuid": "string",
    "leadUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `flowUuid` | string | yes | UUID of the automation. |
| `leadUuid` | string | yes | UUID of the contact to add to the automation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native GetSales.io API, this operation is `POST /flows/api/flows/{flowUuid}/leads/{leadUuid}` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-to-automation.md) for the provider-specific parameters and requirements.

