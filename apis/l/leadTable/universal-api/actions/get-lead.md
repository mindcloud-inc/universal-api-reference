# LeadTable: Get lead



```
GET https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/get-lead?connectionId=$CONNECTION_ID&leadID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/get-lead?${params}`, {
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
| `leadID` | string | yes | The lead to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `plainDescription` | boolean | no | Return a plain-text description instead of HTML when supported. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lead": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lead` | object | Lead record. |

## Native endpoint

Through the native LeadTable API, this operation is `GET /lead/{leadID}` (base URL `https://api.lead-table.com/api/v3/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

