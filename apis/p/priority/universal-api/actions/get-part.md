# Priority: Get Part

Retrieves a part from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-part
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-part?connectionId=$CONNECTION_ID&partName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "partName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-part?${params}`, {
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
| `partName` | string | yes | Priority part key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "PARTDES": "string",
      "PARTNAME": "Ava Chen",
      "PUNITNAME": "Ava Chen",
      "STATDES": "string",
      "TYPE": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `PARTDES` | string |  |
| `PARTNAME` | string |  |
| `PUNITNAME` | string |  |
| `STATDES` | string |  |
| `TYPE` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /PART(PARTNAME=':partName')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-part.md) for the provider-specific parameters and requirements.

